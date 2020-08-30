{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "name": "02-python-101.ipynb",
      "provenance": [],
      "collapsed_sections": []
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "08kwxxPkA2XI",
        "colab_type": "text"
      },
      "source": [
        "## **Densidad poblacional**\n",
        "\n",
        "\n",
        "De acuerdo con información recabada por [INEGI](https://www.inegi.org.mx/temas/estructura/) en 2015, la población para la alcaldía Benito juárez, la CDMX y México eran de:\n",
        "\n",
        "*   Benito Juárez: 385 439 habitantes\n",
        "*   CDMX: 8 998 653 habitantes\n",
        "*   México: 119 530 753 habitantes\n",
        "\n",
        "Por otra parte, las superficies de cada uno de ellos son:\n",
        "\n",
        "*   Benito Juárez: 26,63 km2\n",
        "*   CDMX: 1 495 km2\n",
        "*   México: 1 959 248 km2\n",
        "\n",
        "Para encontrar la densidad de población aplicamos la fórmula:\n",
        "\n",
        "![densidad.jpg](data:image/jpeg;base64,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FNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksggIFNksoPDJ0rKPF3H/dNJ/FU/wA6upv961dINnyWUuLx+qaT+Ko/N1K5X52NcOl0Hw9P+Va6KP1VCijPoqV49NfiPD1Z9vwYzvVfn/zDl/4Yt+UVgYzvVf8A7w5e+GLflFnL/cpMb61TTiIi+iuLEREBERAREQEREBERAREQEREBEWc+Ou3FoMGqcRosWlw2XD4ZJ3MjjY9lQOhj+VvYjospM6LDRiLq48nbx2MdxLG34Zilc6cT07nUwljbG5s7Wh1hoa0lr2bWjp3hdoUoJFhvTUmHlRdaHDJmzOkedIMt0eYp+SrYo6oPfBCTTwyF5kaz0bv0RsLhe1t635LiQw3DnTVFS+obSU7pZql4AfKI2XL9DLNF/ZP/ADU1XR9miyTwWY3mDNtGcSbiM2A0csz+YR00TJJ5adtgyWfldjdXsDYV+ngn4x1fBmGoyriel9W1nOMOq2bOe0uh5HLM9VjzyZOzftTcbWrURFpkREQflZIb2J2noJtb+H0W6lya/Ze46do2AH37XLLnlBuDqjqMv4hiL3Sx1eH0kklJLDUSwFsgNxdkbmtkO07Xg/JfC+SgwOtGX5ayeaWZ9XVOfEZpXSEQsZpDQZCSGud6VhsvtWNWtPDcqIi2yIiICIvS45h0ssMsTJnwSPY9jJmgOfEXbA9jfVc5u8EnUFB7pF1Jf/FbPcmcHZXizFUSRtqOTdVinhL2Qloe6RzNOn0Rsv0LtNyhhU0FNDDLUvq5Y42tkqZGhkkzje7ntbsY47NymqzGj6BERaQREQF+R8tgTfZa972Nrb9ukNX618/mrLkNbTTUsoLoZ2aH6XmMuYdvoSMIc127aCCpI9trNh6W09WwH4XDiv1LqS4BsgTN4TKvD4Kmp824XUTOdDJVSSBsbae+l13kPAl2AG4GzqXbapCzGj8pnsQL7924D7iblfqWA+GngKzRiee6Ksa2ohwOn5qXSR1OiEmMapWljXC+t/oOBadQ2Fb8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ft/umm8SdzgXOrx7Q05dLrMenM/b/dNN4k05n7f7ppvEnc4Fzq8e0NOXS6zHpzP2/wB003iTTmft/umm8SdzgXOrx7Q05dLrMenM/b/dNN4k05n7f7ppvEnc4Fzq8e0NOXS6zHpzP2/3TTeJNOZ+3+6abxJ3OBc6vHtDTl0usx6cz9v9003iTTmft/umm8SdzgXOrx7Q05dLrMenM/b/AHTTeJNOZ+3+6abxJ3OBc6vHtDTl0usx6cz9v9003iTTmft/umm8SdxgXTq8e3+2l5P9xWUeLx+qaT+Ko/N1K9uYszn/AOf9003iX7ODfJgoKSnoxKZuRBBkLdD5HmUyFwYPRa03dfr1HrXi/JZzDzFMU0/x6Xx+WrwJma/6sKj9Vcl+qjozpCL+KMOrT0/onEjV+/GIB1L5mppG33f4O/71CLeej/NjKT4eMUTepTzFvUpRfw7KbPT3SjmDU5g1SibKbJum6OYNTmDVKJspsbpujmDU5g1SibKbG6bo5g1OYNUomymxum6OYNTmDVKJspsbpujmDU5g1SibKbG6bo5g1OYNUomymxum6OYNTmDVKJspsbpujmDU5g1SibKbG6bo5g1OYNUomymxum6OYNTmDVKJspsbpujmDU5g1SibKbG6bo5g1OYNUomymxum6OYNTmDVKJspsbpujmDU5g1SibKbG6bo5g1OYNUomymxum6OYNTmDVKJspsbpujmDU5g1SibKbG6bo5g1OYNUomymxum6OYNTmDVKJspsbpujmDU5g1SibKbG6bo5g1OYNUomymxum6OYNTmDVKJspsbpujmDU5g1SibKbG6bo5g1OYNUomymxum6OYNTmDVKJspsbpujmDU5g1SibKbG6bo5g1OYNUomymxum6OYNTmDVKJspsbpujmDU5g1SibKbG6bo5g1OYNUomymxum6OYNTmDVKJspsbpujmDU5g1SibKbG6bo5g1OYNUomymxum7wikavZUdK3d0bvlZSi/vwaKbM4szo+lp4xYIiL3opjRz1U+X/2Q==)"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "VTJ6VeXZ6dnj",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "def densidad(poblacion,superficie):\n",
        "  return poblacion/superficie\n"
      ],
      "execution_count": 5,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Ys8O9ngCA2p1",
        "colab_type": "text"
      },
      "source": [
        "Entonces para calcular la densidad de la alcaldía Benito Juárez, la CDMX y México, se definen las variables con los valores de población y superficie para cada entidad y se utiliza la función densidad mencionada."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "kjIaZfNT6nmr",
        "colab_type": "code",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        },
        "outputId": "8a319e05-1b46-47b1-98ac-ca0ea9c7f34a"
      },
      "source": [
        "pob_bj = 385439.00\n",
        "sup_bj = 26.63\n",
        "pob_cdmx = 8855000.00\n",
        "sup_cdmx = 1495.00\n",
        "pob_mx = 119530753.00\n",
        "sup_mx = 1959248.00\n",
        "\n",
        "den_bj = densidad(pob_bj,sup_bj)\n",
        "den_cdmx = densidad(pob_cdmx,sup_cdmx)\n",
        "den_mx = densidad(pob_mx,sup_mx)\n",
        "\n",
        "str_den = \"La alcaldía Benito Juárez: {:.2} hab/km2\\nCDMX: {:.2} hab/km2\\nMéxico: {:.4} hab/km2\"\n",
        "print(str_den.format(den_bj, den_cdmx, den_mx))\n"
      ],
      "execution_count": 10,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "La alcaldía Benito Juárez: 1.4e+04 hab/km2\n",
            "CDMX: 5.9e+03 hab/km2\n",
            "México: 61.01 hab/km2\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "fQBnxSDQA2st",
        "colab_type": "text"
      },
      "source": [
        "**¿Cuál es la densidad poblacional?**\n",
        "\n",
        "\n",
        "\n",
        "*   Benito Juárez: 1 400 hab/km2\n",
        "*   CDMX: 5 900 hab/km2\n",
        "*   México: 61.01 hab/km2\n",
        "\n",
        "**¿Qué pasa comparar varios estados o ciudades?**\n",
        "\n",
        "Podemos observar las diferencias entre medir una alcaldía, una ciudad y un país. \n",
        "\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Xd28H39-XU2u",
        "colab_type": "text"
      },
      "source": [
        "#**Gasto Público**\n",
        "\n",
        "Para calcular el gasto público se utilizó información de la página [\"Transparencia Presupuestaria\"](https://www.transparenciapresupuestaria.gob.mx/) y se descubrió que en 2019 se destinaron 746,742.8 mdp. Mientras que en 2018, se destinaron 737,720.1 mdp. Para encontrar el gasto per cápita es necesario dividir el total de gasto entre el número de habitantes. "
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "0sTYvQV_8tUU",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "def per_capita(gasto, poblacion):\n",
        "  return gasto / poblacion"
      ],
      "execution_count": 11,
      "outputs": []
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "AS5sSMvh8xsM",
        "colab_type": "code",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        },
        "outputId": "46f0461e-e077-462e-9c54-82d01f3ace02"
      },
      "source": [
        "ed_2018 = 737720100000\n",
        "ed_2019 = 746742800000\n",
        "pob_2018 = 124700000\n",
        "pob_2019 = 125930000\n",
        "\n",
        "ed_pc_18 = per_capita(ed_2018, pob_2018)\n",
        "ed_pc_19 = per_capita(ed_2019, pob_2019)\n",
        "\n",
        "print(\"2018: {:.6}\\n2019: {:.6}\".format(ed_pc_18, ed_pc_19))"
      ],
      "execution_count": 12,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "2018: 5915.96\n",
            "2019: 5929.82\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "G-sdffRlXM8Z",
        "colab_type": "text"
      },
      "source": [
        "Para calcular el porcentaje, utilizamos la siguiente función:\n"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "8dqdt8Yh85z2",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "def porcentaje(a, b):\n",
        "  return (b - a) / b * 100"
      ],
      "execution_count": 13,
      "outputs": []
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "5SAvtlJg86fW",
        "colab_type": "code",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        },
        "outputId": "a274f308-4622-4b54-9766-c380be71f17d"
      },
      "source": [
        "cambio = porcentaje(ed_pc_18, ed_pc_19)\n",
        "\n",
        "print(\"Hubo un aumento del {:.2}%\".format(cambio))"
      ],
      "execution_count": 14,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Hubo un aumento del 0.23%\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "3hffeqC2YAkT",
        "colab_type": "text"
      },
      "source": [
        "**¿En qué porcentaje aumentó o disminuyó?**\n",
        "\n",
        "El Gasto Público aumentó un 0.23%\n",
        "\n",
        "**¿A qué crees que se deba?**\n",
        "\n",
        "Considero que este aumento tan pequeño, se debe a que el Gobierno Federal decidió incrementar en sectores específicos, en un porcentaje moderado, los presupuestos.\n",
        "\n",
        "Preguntas finales:\n",
        "\n",
        "**¿Para qué crees que nos pueda ser útil esta información?**\n",
        "\n",
        "Como ciudadanos es importante conocer en qué se utiliza el dinero obtenido a través de la recaudación fiscal. Esto permite conocer las prioridades del gobierno en turno.\n",
        "\n",
        "**¿Qué decisiones podría tomar el gobierno basado en ésta?**\n",
        "\n",
        "Debido a la condición actual que estamos pasando, el gobierno podría usar la información del gasto para contener los efectos que la contingencia podría tener en la economía."
      ]
    }
  ]
}