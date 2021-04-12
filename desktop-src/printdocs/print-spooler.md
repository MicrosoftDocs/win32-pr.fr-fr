---
description: Le composant principal de l’interface d’impression est le spouleur d’impression.
ms.assetid: 36ffb001-78e2-4fa0-8241-3891493ac02d
title: Spouleur d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfcc6ea2e46c06b5e51032a4c43f46df7f07c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529175"
---
# <a name="print-spooler"></a>Spouleur d’impression

Le composant principal de l’interface d’impression est le spouleur d’impression. Le spouleur d’impression est un fichier exécutable qui gère le processus d’impression. La gestion de l’impression implique la récupération de l’emplacement du pilote d’imprimante approprié, le chargement de ce pilote, la mise en file d’attente des appels de fonctions de haut niveau dans un travail d’impression, la planification du travail d’impression pour l’impression, etc. Le spouleur est chargé au démarrage du système et continue à s’exécuter jusqu’à ce que le système d’exploitation soit arrêté.

Les applications qui impriment créent un contexte de périphérique d’impression (DC). Quand une application crée un DC d’imprimante, le spouleur effectue les tâches nécessaires, telles que la détermination de l’emplacement du pilote d’imprimante requis, puis le chargement de ce pilote. Le spouleur d’impression détermine également le type de données utilisé pour enregistrer le travail d’impression.

Le spouleur d’impression prend en charge les types de données suivants :

-   Métafichier amélioré (EMF).
-   Texte ASCII.
-   Données brutes, qui incluent des types de données d’imprimante tels que PostScript, PCL et des types de données personnalisés.

Les types de données personnalisés peuvent être ajoutés au spouleur en installant des pilotes d’imprimante et des processeurs d’impression supplémentaires. Un travail d’impression est un document stocké en interne et encodé à l’aide de l’un des types de données pris en charge, et un travail d’impression peut contenir une ou plusieurs pages de sortie. Le travail d’impression peut être constitué de plusieurs formulaires. par exemple, un travail peut se composer d’une enveloppe et de trois pages de papier A4. Un travail d’impression est défini (ou placé entre crochets) par les fonctions [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) et [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .

Le type de données par défaut pour un travail d’impression est le métafichier amélioré. Un enregistrement EMF est une structure compacte utilisée pour stocker des commandes de sortie de texte, des commandes graphiques raster, et ainsi de suite. Quand une application appelle [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca), le spouleur crée un fichier de mise en file d’attente et un fichier de données et commence à stocker les enregistrements EMF dans le fichier de mise en file d’attente. Chaque fois que l’application appelle l’une des fonctions de dessin GDI, un ou plusieurs nouveaux enregistrements EMF sont créés et stockés dans le fichier de mise en file d’attente. Les fichiers de mise en file d’attente et de données sont créés dans un répertoire du système d’exploitation. Le spouleur utilise le fichier de mise en file d’attente pour stocker les enregistrements EMF et utilise le fichier de données pour enregistrer le type de formulaire, le type de données du travail d’impression, l’imprimante cible, et ainsi de suite. Le spouleur supprime ces fichiers une fois que le travail a été correctement imprimé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fichiers de format amélioré](/windows/desktop/gdi/enhanced-format-metafiles)
</dt> </dl>

 

 
