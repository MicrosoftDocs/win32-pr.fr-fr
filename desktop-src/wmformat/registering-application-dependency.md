---
title: inscription de la dépendance d’Application (kit de développement logiciel (SDK) Windows Media Format 11)
description: découvrez comment inscrire votre application avec les composants d’exécution des api fournies par le kit de développement logiciel (SDK) Windows Media Format 11.
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK, inscrire des dépendances d’application
- inscription des dépendances d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd546ee9b162652f00a131e87561a7e34f7e3a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521065"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a>inscription de la dépendance d’Application (kit de développement logiciel (SDK) Windows Media Format 11)

les Applications qui utilisent des api fournies par le kit de développement logiciel (sdk) Windows Media Format ou Lecteur Windows Media sdk dépendent des composants d’exécution de ces technologies. Vous pouvez inscrire votre application comme étant dépendante de ces composants dans le cadre de la configuration de votre application.

Lorsque vous inscrivez votre application, vous pouvez choisir l’un des deux niveaux de dépendance : blocage ou dépendant. Quand une ou plusieurs applications sont inscrites avec une dépendance de blocage sur l’un des composants d’exécution, le composant est bloqué d’une restauration vers une version antérieure. Les applications dépendantes qui ne sont pas inscrites comme bloquantes ne bloquent pas la restauration. Au lieu de cela, avant d’effectuer la restauration, l’utilisateur est invité à entrer un message indiquant que les applications sont dépendantes du composant.

Pour inscrire votre application, vous devez définir une valeur dans le Registre qui identifie votre application. La valeur de Registre à définir dépend du composant dont dépend votre application. Vous pouvez également définir deux valeurs supplémentaires par dépendance pour fournir des informations supplémentaires sur votre application.

les valeurs de registre suivantes sont utilisées pour inscrire la dépendance sur le runtime SDK Windows Media Format :

-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ installation \\ *\_ type de référence* \\ application, «*application*»,*« \_ chaîne d’application*»
-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ - \\ *\_* \\ descripteur de type de référence, "*application*", "*\_ descripteur de référence*"
-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ installation \\ *\_ type de référence* \\ version,*application*, «*\_ version WMF*»

la valeur de registre suivante est utilisée pour inscrire la dépendance sur Lecteur Windows Media runtime SDK :

-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ MediaPlayer \\ installation \\ *\_ type référence* \\ application, «*application*», «*\_ chaîne d’application*»
-   HKEY \_ classes \_ root \\ Software racine \\ Microsoft \\ MediaPlayer \\ programme d’installation \\ descripteur de *\_ type REF* \\ , "*app*", "*Ref \_ Descriptor*"
-   HKEY \_ classes \_ root \\ Software racine \\ Microsoft \\ MediaPlayer \\ Setup \\ *\_ type REF* \\ , "*app*", "*WMP \_ version*"

Les variables suivantes sont utilisées dans les valeurs de Registre répertoriées ci-dessus :

*TYPE de référence \_*

Remplacez par BlockingRefCounts pour le blocage de la dépendance ou par DependentRefCounts pour une dépendance non bloquante.

*APP*

Nom ou descripteur abrégé de votre application. Cette chaîne ne sera pas utilisée dans les messages affichés pour l’utilisateur. Cette valeur est l’identificateur utilisé dans les trois valeurs de Registre associées à chacun des composants Runtime.

*chaîne d’application \_*

Descripteur de votre application. Cette chaîne peut être utilisée dans les messages affichés pour l’utilisateur.

*descripteur de référence \_*

Description de la façon dont votre application utilise le composant. Cette valeur peut inclure un maximum de 256 caractères.

*VERSION de WMP \_*

Version de Lecteur Windows Media requise par votre application.

*\_version WMF*

Version du kit de développement logiciel (SDK) Windows Media Format requis par votre application.

Les trois exemples de valeurs de registre suivants montrent comment configurer les valeurs de votre application :

-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ Setup \\ DependentRefCounts \\ application, "southridgevideo", "Southridge Video Player"
-   HKEY \_ CLASSES \_ racine \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ Descriptor, "SouthridgeVideo", "Southridge video Player utilise le kit de développement logiciel (SDK) Windows media Format pour lire les fichiers vidéo."
-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ Setup \\ DependentRefCounts \\ version, "southridgevideo", "9.0.0.2600"

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Project Raisons**](project-considerations.md)
</dt> </dl>

 

 




