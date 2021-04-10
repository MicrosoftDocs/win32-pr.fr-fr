---
title: À propos des contrôles Month Calendar
description: Un contrôle Month Calendar implémente une interface utilisateur de type calendrier.
ms.assetid: 81b8f233-272e-4043-92ff-5ff47b0610d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f61b0ffc291473b330469910d1dad0317668e1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102417"
---
# <a name="about-month-calendar-controls"></a>À propos des contrôles Month Calendar

Un contrôle Month Calendar implémente une interface utilisateur de type calendrier. Cela fournit à l’utilisateur une méthode très intuitive et reconnaissable pour entrer ou sélectionner une date. Le contrôle fournit également à l’application la possibilité d’obtenir et de définir les informations de date dans le contrôle à l’aide des types de données existants.

-   [Fonctionnalités du contrôle Month Calendar](#month-calendar-control-features)
    -   [Sélection d’un jour](#selecting-a-day)
    -   [Sélection d’un mois non adjacent](#selecting-a-nonadjacent-month)
    -   [Sélection d’une autre année](#selecting-a-different-year)
-   [Localisation](#localization)
-   [Heures dans le contrôle Month Calendar](#times-in-the-month-calendar-control)

## <a name="month-calendar-control-features"></a>Fonctionnalités du contrôle Month Calendar

La capture d’écran suivante montre un contrôle Month Calendar qui a été dimensionné pour afficher deux mois.

![capture d’écran d’une boîte de dialogue avec un contrôle Month Calendar montrant deux mois, côte à côte](images/mc-simple.png)

> [!Note]  
> L’apparence et le comportement du contrôle Month Calendar diffère légèrement sous les différentes versions de la bibliothèque Runtime. Cette rubrique se concentre sur le contrôle tel qu’il apparaît dans Windows Vista avec la version 6 de Comctl32.dll.

 

Le contrôle de l’illustration présente les fonctionnalités facultatives suivantes.

-   La date du jour est indiquée sur une ligne distincte au bas du contrôle. Il s'agit du style par défaut.
-   Le « cercle aujourd’hui » (en réalité un rectangle dans cette version) apparaît autour du jour actuel et en regard de la ligne « aujourd’hui » comme un signal visuel. Il s'agit du style par défaut.
-   Les numéros de semaine s’affichent à gauche de chaque ligne de jours. Ce style doit être spécifié.
-   Certaines dates sont affichées en gras, en fonction de l’état du jour défini par l’application. Par exemple, les dates qui ont des réunions planifiées peuvent être affichées en gras. Ce style doit être spécifié.

> [!Note]
>
> Windows ne prend pas en charge les dates antérieures à 1601. Pour plus d’informations, consultez [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .
>
> Le contrôle Month-Calendar est basé sur le calendrier grégorien, qui a été introduit dans 1753. Elle ne calcule pas les dates qui sont cohérentes avec le calendrier julien qui était utilisé avant 1753.

 

### <a name="selecting-a-day"></a>Sélection d’un jour

Par défaut, lorsqu’un utilisateur clique sur les boutons de direction situés en haut à gauche ou en haut à droite du contrôle Month Calendar, le contrôle met à jour son affichage pour afficher le mois précédent ou suivant. L’utilisateur peut également effectuer la même action en cliquant sur les mois partiels affichés avant le premier mois et après le mois dernier.

Les commandes clavier suivantes peuvent également être utilisées pour déplacer la sélection. Le calendrier défile toujours en fonction des besoins pour afficher le jour sélectionné. (Les [**codes de touche virtuelle**](/windows/desktop/inputdev/virtual-key-codes) sont affichés dans le tableau.)



|                         |                                                                                                                                                                                                                                          |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flèche gauche (VK \_ gauche)   | Sélectionnez le jour précédent.                                                                                                                                                                                                                 |
| Flèche droite (VK \_ Right) | Sélectionnez le jour suivant.                                                                                                                                                                                                                     |
| Flèche haut (VK \_ up)       | Sélectionnez le même jour de la semaine précédente.                                                                                                                                                                                                |
| Flèche bas (VK \_ Bas)   | Sélectionnez le même jour de la semaine suivante.                                                                                                                                                                                                    |
| PAGE précédente (VK \_ précédent)     | Sélectionnez le même jour du mois précédent. (Si ce mois n’a pas le jour, le jour le plus proche est sélectionné ; par exemple, la sélection se déplace du 31 mars au 28 février ou 29 février.)                                                      |
| PAGE suivante (VK \_ suivant)    | Sélectionnez le même jour du mois suivant.                                                                                                                                                                                                   |
| Page d’hébergement (VK \_ )         | Sélectionnez le premier jour du mois en cours.                                                                                                                                                                                               |
| FIN ( \_ fin VK)           | Sélectionnez le dernier jour du mois en cours.                                                                                                                                                                                                |
| CTRL + DÉBUT             | Faites défiler d’un mois vers l’arrière et sélectionnez un jour dans la colonne la plus à gauche.                                                                                                                                                                       |
| CTRL + FIN              | Faites défiler vers l’avant un mois et sélectionnez un jour dans la colonne la plus à droite.                                                                                                                                                                       |
| CTRL + PG. HAUT          | Sélectionnez le même jour dans un mois précédent. Le nombre de mois de déplacement de la sélection est le nombre de mois affichés dans le contrôle. Par exemple, si deux mois s’affichent, la sélection se déroulera du 6 juin au 6 mai.    |
| CTRL + PG. SUIV.        | Sélectionnez le même jour dans un mois précédent. Le nombre de mois de déplacement de la sélection est le nombre de mois affichés dans le contrôle. Par exemple, si deux mois s’affichent, la sélection se déroulera du 6 juin au 6 août. |



 

Si un contrôle Month Calendar n’utilise pas le style [**MCS \_ notoday**](month-calendar-control-styles.md) , l’utilisateur peut retourner au jour actuel en cliquant sur le texte « Today » en bas du contrôle. Si le jour actuel n’est pas visible, le contrôle met à jour son affichage pour l’afficher.

Une application peut modifier le nombre de mois pendant lesquels le contrôle met à jour son affichage à l’aide du message [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) ou de la macro correspondante, [**calendrier monthcal \_ SETMONTHDELTA**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta). Toutefois, les touches PAGE précédente et PAGE suivante modifient le mois sélectionné d’une unité, quel que soit le nombre de mois affichés ou la valeur définie par **MCM \_ SETMONTHDELTA**.

### <a name="selecting-a-nonadjacent-month"></a>Sélection d’un mois non adjacent

Lorsqu’un utilisateur clique sur le nom d’un mois affiché, tous les mois de l’année sont répertoriés (dans les versions antérieures, il s’agit d’un menu contextuel). L’utilisateur peut sélectionner un mois dans la liste. Si la sélection de l’utilisateur n’est pas visible, le contrôle Month Calendar fait défiler son affichage pour afficher le mois choisi. Dans la capture d’écran suivante, un contrôle Month Calendar affiche les mois de deux années adjacentes.

![capture d’écran d’une boîte de dialogue avec un contrôle Month Calendar montrant tous les mois de 2007 et 2008](images/mc-months.png)

### <a name="selecting-a-different-year"></a>Sélection d’une autre année

Si l’utilisateur clique sur l’année, un groupe d’années est répertorié et l’utilisateur peut en sélectionner un autre, comme illustré dans la capture d’écran suivante.

![capture d’écran d’un contrôle Month Calendar montrant toutes les années comprises entre 1999 et 2020](images/mc-years.png)

## <a name="localization"></a>Localisation

Le contrôle Month-Calendar obtient son format et toutes les chaînes des paramètres \_ régionaux \_ par défaut de l’utilisateur.

## <a name="times-in-the-month-calendar-control"></a>Heures dans le contrôle Month Calendar

Le contrôle Month Calendar n’affiche pas l’heure. Toutefois, la structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) utilisée pour définir et récupérer la date sélectionnée ou la date du jour contient des champs d’heure. Quand une date est définie par programme, le contrôle copie les champs d’heure tels quels ou les valide en premier, puis, s’ils ne sont pas valides, stocke les heures par défaut actuelles. Voici une liste des messages qui définissent une date et une description de la façon dont les champs d’heure sont traités.



|                                             |                                                                                                                                                                                                                            |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCM \_ SETCURSEL**](mcm-setcursel.md)     | Le contrôle copie les champs d’heure tels quels, sans validation ni modification.                                                                                                                                        |
| [**MCM \_ SEtrange**](mcm-setrange.md)       | Les champs d’heure des structures passées sont validés. S’ils sont valides, les champs d’heure sont copiés sans modification. Si elles ne sont pas valides, le contrôle copie les champs d’heure à partir des données d’aujourd’hui.                  |
| [**MCM \_ SETSELRANGE**](mcm-setselrange.md) | Les champs d’heure des structures passées sont validés. S’ils sont valides, les champs d’heure sont copiés sans modification. Si elles ne sont pas valides, le contrôle conserve les champs d’heure des plages de sélection actuelles. |
| [**MCM \_ SETTODAY**](mcm-settoday.md)       | Le contrôle copie les champs d’heure tels quels, sans validation ni modification.                                                                                                                                        |



 

Lorsqu’une date est récupérée à partir du contrôle, les champs d’heure sont copiés à partir des heures stockées sans modification. La gestion des champs d’heure par le contrôle est fournie à titre de commodité au programmeur. Le contrôle n’examine pas ou ne modifie pas les champs d’heure à la suite d’une opération autre que celles listées ci-dessus.

 

 