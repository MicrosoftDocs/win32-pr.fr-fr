---
title: Migration des pilotes Graphics vers Windows 10
description: Windows 10 les éléments multimédias et Windows 10, comme son prédécesseur, Windows 8.1, n’ont pas de pilotes graphiques tiers dans le kit multimédia Windows ou « in Box ».
ms.assetid: E6240CF0-5A65-4A66-98AE-856C783EB320
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b1703210318f55dad3e50f4dcdd7e143434275b7ef3b41203f41792262a53e5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882709"
---
# <a name="graphics-driver-migration-to-windows-10"></a>Migration des pilotes Graphics vers Windows 10

Windows 10 les éléments multimédias et Windows 10, comme son prédécesseur, Windows 8.1, n’ont pas de pilotes graphiques tiers dans le kit multimédia Windows ou « in Box ». Au lieu de cela, les pilotes graphiques pour un large éventail d’appareils sont approvisionnés sur WU, ce qui permet aux fournisseurs de matériel de mettre à jour les pilotes sans nécessiter de modification de l’image du système d’exploitation. en outre, les pilotes existants ne sont pas migrés vers Windows 10 lors d’une mise à niveau du système d’exploitation vers Windows 10 à partir de Windows 7, Windows 8 ou Windows 8.1. Cela a également un impact sur les mises à niveau de Windows Server 2012.

## <a name="upgrades-and-installation"></a>Mises à niveau et installation

pour les mises à niveau et les nouvelles installations, les pilotes graphiques doivent être obtenus à partir de Windows Update (WU) ou du site web IHV/OEM pour le matériel concerné. Vous avez besoin pour cela d'une connexion Internet. les pilotes sur WU sont injectés dans le programme d’installation du système d’exploitation par la mise à jour dynamique (DU) lorsqu’un utilisateur met à niveau son Windows 7 ou Windows 8 système. x sur Windows 10.

> [!Note]  
> cela ne s’applique pas aux systèmes fournis avec Windows préinstallés, par exemple les ordinateurs prêts à l’emploi achetés dans un magasin de vente au détail. Ces systèmes disposent déjà des pilotes graphiques installés par l’OEM. L’OEM peut également fournir un DVD (pour réinstaller le système d’exploitation) qui comprend les pilotes.

 

après la mise à niveau vers Windows 10, les utilisateurs peuvent constater qu’aucun pilote graphique n’est installé sur leur ordinateur. Cela peut se produire pour les raisons suivantes :

-   L’utilisateur a choisi d’effectuer une nouvelle installation, c’est-à-dire pas une mise à niveau.
-   L’utilisateur a sélectionné l’option de vérification des mises à jour lors de la mise à niveau, c.-à-d. une mise à jour dynamique effectivement désactivée (DU).
-   La connexion Internet ne fonctionnait pas pendant la mise à niveau.
-   L’installation du pilote a échoué.

Après une nouvelle installation du système d’exploitation, aucun pilote graphique n’est présent sur l’ordinateur tant que le client WU n’est pas exécuté automatiquement et téléchargé les pilotes applicables. À l’intérim, le PC exécutera la MSBDA (Microsoft Basic Display Adapter), qui offre des fonctionnalités limitées, par exemple aucune prise en charge de plusieurs moniteurs, et l’utilisateur peut également rencontrer une baisse des performances par rapport à un pilote matériel, par exemple une fréquence d’images lente ou une déchirure de la lecture vidéo.

## <a name="manifestations"></a>Manifestations

pour les pc plus anciens (généralement créés avant le Windows 7), il est possible qu’il n’existe aucun pilote pour Windows 10 sur WU, car les cartes graphiques ont atteint leur fin de vie (EOL) et ne sont plus prises en charge par les fournisseurs de matériel. même les systèmes en cours d’exécution Windows 7 ou 8. x peuvent avoir été mis à niveau à partir d’un système d’exploitation antérieur et peuvent avoir des cartes graphiques EOL.

Des pilotes récents peuvent ne pas être disponibles, car la carte graphique a été transférée à partir d’un ancien ordinateur, par exemple lors d’une mise à niveau matérielle. Cela se produit le plus souvent pour les ordinateurs dotés de plusieurs cartes graphiques, où l’utilisateur a conservé une ancienne carte graphique lors de l’achat d’un nouvel ordinateur afin d’utiliser plusieurs affichages.

une autre possibilité pour un petit pourcentage de machines est que Windows Update possède uniquement des pilotes de « couverture ». Il s’agit de pilotes génériques qui n’ont pas de personnalisations OEM. un utilisateur qui a remis l’un de ces pilotes après la mise à niveau vers Windows 10 peut constater que certaines fonctionnalités sont manquantes, par exemple les touches de fonction pour contrôler la luminosité de l’écran ne fonctionnent plus.

## <a name="mitigations"></a>Corrections

-   Les pilotes graphiques appropriés doivent être remis par le pendant le processus de mise à niveau ou par WU peu après la fin de la mise à niveau. les oem doivent s’assurer que les pilotes graphiques appropriés sont inclus dans les images système utilisées pour l’installation usine de Windows 10 sur leurs ordinateurs.
-   après une mise à niveau, l’utilisateur peut vérifier explicitement Paramètres \\ Windows Update pour les pilotes, bien que cela ne soit pas nécessaire. Les utilisateurs qui forcent une vérification lorsqu’un pilote est installé automatiquement en arrière-plan peuvent voir un échec d’installation du pilote si l’installation automatique se termine en premier. Vous pouvez ignorer ce message.
-   les utilisateurs qui envisagent d’effectuer une nouvelle installation de Windows 10 doivent obtenir les pilotes appropriés avant d’installer ou s’appuyer sur Windows Update pour fournir les pilotes ultérieurement. dans ce cas, ils doivent s’assurer que leur connexion Internet fonctionne.
-   Pour les ordinateurs qui reçoivent un pilote de couverture, il n’y a pas d’atténuation pour les fonctionnalités manquantes. Toutefois, cela ne doit se produire que dans les cas où le fournisseur de matériel ne gère plus les pilotes, c’est-à-dire les ordinateurs datant de plusieurs ans.

> [!Note]  
> Pour les systèmes avec un seul affichage, par exemple un ordinateur portable, de nombreux utilisateurs trouvent que MSBDA est acceptable et ne remarquent pas l’absence de pilote matériel. Dans ce cas, aucune atténuation n’est requise.

 

## <a name="solutions"></a>Solutions

il est essentiel que les ihv et les oem chargent leurs pilotes graphiques Windows 10 dans WU pour tout matériel qu’ils envisagent de prendre en charge.

Les utilisateurs doivent conserver l’option « vérifier les mises à jour » sélectionnée (paramètre par défaut) lors de la mise à niveau. Selon la vitesse de la connexion réseau et la charge sur les serveurs WU, cela peut signifier que les pilotes ne sont pas installés tant que OOBE n’est pas terminé et que l’utilisateur s’est connecté pour la première fois. En attendant, l’utilisateur peut remarquer des fonctionnalités limitées ou des performances médiocres.

Les utilisateurs doivent s’assurer que leur connexion Internet fonctionne avant de commencer une mise à niveau, même si elles sont en cours de mise à niveau à l’aide d’un média (DVD ou lecteur flash).

-   Si le PC est connecté à Internet, les pilotes appropriés doivent être téléchargés et installés automatiquement. L’utilisateur n’a pas besoin d’effectuer aucune action.
-   Si le PC n’est pas connecté à Internet, les pilotes doivent être téléchargés à partir du IHV ou du site Web OEM à l’aide d’un ordinateur connecté à Internet ; transféré vers l’ordinateur cible à l’aide d’un lecteur flash ou d’un CD/DVD ; puis installé manuellement.

 

 




