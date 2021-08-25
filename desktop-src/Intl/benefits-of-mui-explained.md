---
description: Explication des avantages de l’interface MUI
ms.assetid: 5b9851e0-4354-4088-b099-0f5f5fac4a35
title: Explication des avantages de l’interface MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971f66ef7fc094912e87d7e9ab77284fecb0931d9222e6910931b281b6308286
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829698"
---
# <a name="benefits-of-mui-explained"></a>Explication des avantages de l’interface MUI

-   [Avantages MUI pour les développeurs](#mui-benefits-for-developers)
-   [Avantages MUI pour les entreprises](#mui-benefits-for-enterprises)
-   [Avantages MUI pour les OEM](#mui-benefits-for-oems)

## <a name="mui-benefits-for-developers"></a>Avantages MUI pour les développeurs

Il existe de nombreuses façons d’implémenter une solution MUI dans des applications, mais chaque possibilité est une variante de l’une des trois méthodes de base :

1.  Compilation d’un fichier binaire (avec les ressources intégrées) pour chaque langue. Il s’agit *de la norme de facto* pour les applications héritées, car il s’agit du modèle principal pris en charge par les outils de développement standard, tels que les Microsoft Visual Studio. Ce modèle requiert plusieurs binaires pour plusieurs langues et présente des limitations en ce qui concerne le déploiement d’une image unique et les scénarios multilingues. il convient de noter que les applications développées à l’aide de ce modèle continueront de fonctionner sur Windows Vista et que des outils sont fournis pour aider les développeurs à passer de ce modèle au modèle plus moderne présenté dans la troisième méthode.
2.  Avoir un binaire de base indépendant de la langue avec une bibliothèque de liens dynamiques (DLL) de ressources multilingues. Ce modèle est sans aucun doute convivial, mais il rend difficile la mise à jour des binaires de ressources pour prendre en charge de nouvelles langues. Supposons que, outre l’anglais, le français et le japonais, vous souhaitez également prendre en charge l’allemand. Un nouveau fichier binaire de ressource doit être fourni et déployé à vos utilisateurs qui n’ont peut-être pas forcément besoin de l’allemand.
3.  Avoir un binaire de base indépendant du langage avec un ensemble de dll de ressource par langue. il s’agit de la façon dont le système d’exploitation lui-même est implémenté dans Windows Vista, et les développeurs sont encouragés à utiliser ce modèle pour les applications, car il offre plus que les deux modèles précédents.

avant la version Windows Vista, l’absence de prise en charge intégrée de ce dernier modèle rendait difficile l’adoption. Toutefois, cela a changé et les avantages de ce modèle sont nombreux et en font un excellent modèle pour vos applications :

-   les Applications peuvent être multilingues et peuvent se comporter de la même façon que Windows Vista, offrant ainsi une expérience de langue d’affichage cohérente pour les utilisateurs.
-   La flexibilité est accrue dans la publication de langues supplémentaires pour une application. Des langues supplémentaires peuvent être libérées indépendamment du code de base, ce qui signifie que la prise en charge de nouvelles langues peut être ajoutée au fil du temps en fonction des besoins.
-   Le coût est réduit lors de la création et de la maintenance de versions linguistiques supplémentaires.
-   Les OEM et les entreprises peuvent facilement intégrer des applications dans leur image de PC globalisée, prêts à être expédiés dans différents pays.
-   les outils et les instructions qui vous aident à migrer votre application vers le modèle MUI Windows Vista sont disponibles. En particulier, MSDN fournit un [ensemble important de documentation](multilingual-user-interface.md) sur MUI.

## <a name="mui-benefits-for-enterprises"></a>Avantages MUI pour les entreprises

MUI offre deux principaux avantages pour les entreprises :

-   Installation d’une seule image : MUI permet aux entreprises de déployer, de prendre en charge et de maintenir la même image dans le monde entier (ou une partie de celle-ci) avec une seule installation. Windows Vista étend le déploiement d’une seule image du système d’exploitation afin que les applications métier puissent également être déployées dans le cadre de la même image.
-   Prise en charge des postes de travail multilingues : plusieurs modules linguistiques de l’interface utilisateur localisés peuvent être installés sur un ordinateur de bureau, ce qui permet à plusieurs utilisateurs de partager un même bureau tout en utilisant leurs propres langues d’interface utilisateur préférées. Cela s’applique également aux ordinateurs publics, qui nécessitent un traitement égal pour toutes les langues officiellement parlées (telles que le cas au Canada et dans l’Union européenne) et aux ordinateurs partagés pour les utilisateurs itinérants.

## <a name="mui-benefits-for-oems"></a>Avantages MUI pour les OEM

L’avantage majeur pour les OEM est l’installation d’image unique que MUI active, car il permet de créer des images qui contiennent toutes les langues nécessaires pour cibler une zone géographique efficacement et de retarder le choix de la langue pour l’installation initiale de l’utilisateur de l’ordinateur. En particulier, cela permet une gestion plus efficace de l’inventaire pour les OEM.

grâce à la prise en charge mui des applications, Windows Vista permet également aux oem de fournir des applications à valeur ajoutée sur leurs images tout en bénéficiant de l’installation d’une seule image, à condition que ces applications soient activées pour mui.

 

 



