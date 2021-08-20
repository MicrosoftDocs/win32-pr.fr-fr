---
title: inscription de la dépendance d’Application (kit de développement logiciel Lecteur Windows Media)
description: découvrez comment inscrire votre application avec les composants d’exécution des api fournies par le kit de développement logiciel (SDK) Lecteur Windows Media.
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Lecteur Windows Media, paramètres du registre de dépendances d’application
- Lecteur Windows Media, paramètres du registre de dépendances
- Lecteur Windows Media, registre
- Registre, paramètres de dépendance d’application
- Registre, paramètres de dépendance
- registre, paramètres pour Lecteur Windows Media
- paramètres du registre des dépendances
- paramètres du registre de dépendances d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa210debc4045326eb3bbae1e4fc137db5fb5a5dec6b89e493aedd54f110f82f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861549"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a>inscription de la dépendance d’Application (kit de développement logiciel Lecteur Windows Media)

les Applications qui utilisent des api fournies par le kit de développement logiciel (sdk) Lecteur Windows Media ou Windows Media Format sdk dépendent des composants d’exécution de ces technologies. Vous pouvez inscrire votre application comme étant dépendante de ces composants dans le cadre de la configuration de votre application.

Lorsque vous inscrivez votre application, vous pouvez choisir l’un des deux niveaux de dépendance : blocage ou dépendant. Quand une ou plusieurs applications sont inscrites avec une dépendance de blocage sur l’un des composants du runtime, le composant est bloqué d’une restauration vers une version antérieure. Les applications dépendantes qui ne sont pas inscrites comme bloquantes ne bloquent pas la restauration. Au lieu de cela, avant d’effectuer la restauration, l’utilisateur affiche un message indiquant que les applications dépendent du composant.

Pour inscrire votre application, vous devez définir une valeur dans le Registre qui identifie votre application. La valeur de Registre à définir dépend du composant dont dépend votre application. Vous pouvez également définir deux valeurs supplémentaires par dépendance pour fournir des informations supplémentaires sur votre application.

les valeurs de registre suivantes sont utilisées pour inscrire la dépendance sur Lecteur Windows Media runtime SDK :

-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ MediaPlayer \\ installation \\ *\_ type référence* \\ application, «*application*», «*\_ chaîne d’application*»
-   HKEY \_ classes \_ root \\ Software racine \\ Microsoft \\ MediaPlayer \\ programme d’installation \\ descripteur de *\_ type REF* \\ , "*app*", "*Ref \_ Descriptor*"
-   HKEY \_ classes \_ root \\ Software racine \\ Microsoft \\ MediaPlayer \\ Setup \\ *\_ type REF* \\ , "*app*", "*WMP \_ version*"

les valeurs de registre suivantes sont utilisées pour inscrire la dépendance sur le runtime SDK Windows Media Format :

-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ installation \\ *\_ type de référence* \\ application, «*application*»,*« \_ chaîne d’application*»
-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ - \\ *\_* \\ descripteur de type de référence, "*application*", "*\_ descripteur de référence*"
-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ installation \\ *\_ type de référence* \\ version,*application*, «*\_ version WMF*»

Les variables suivantes sont utilisées dans les valeurs de Registre répertoriées ci-dessus :

*TYPE de référence \_*

Remplacez par BlockingRefCounts pour le blocage de la dépendance ou par DependentRefCounts pour une dépendance non bloquante.

*APP*

Nom ou descripteur abrégé de votre application. Cette chaîne ne sera pas utilisée dans les messages affichés pour l’utilisateur. Cette valeur est l’identificateur utilisé dans les trois valeurs de Registre associées à chacun des composants du Runtime.

*chaîne d’application \_*

Descripteur de votre application. Cette chaîne peut être utilisée dans les messages affichés pour l’utilisateur.

*descripteur de référence \_*

Description de la façon dont votre application utilise le composant. Cette valeur peut inclure un maximum de 256 caractères.

*VERSION de WMP \_*

Version de Lecteur Windows Media requise par votre application. Si aucune version n’est spécifiée, la valeur par défaut est supposée être 9.0.0.0.

*\_version WMF*

Version du kit de développement logiciel (SDK) Windows Media Format requis par votre application.

Les trois exemples de valeurs de registre suivants montrent comment configurer les valeurs de votre application :

-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ MediaPlayer \\ programme d’installation \\ DependentRefCounts \\ , « southridgevideo », « lecteur vidéo Southridge »
-   HKEY \_ CLASSES \_ ROOT \\ Software racine \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Descriptor, « SouthridgeVideo », « Southridge video Player utilise le kit de développement logiciel (SDK) de Format multimédia Windows pour lire des fichiers vidéo ».
-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ MediaPlayer \\ programme d’installation \\ DependentRefCounts \\ , « southridgevideo », « 9.0.0.2600 »

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres du Registre**](registry-settings.md)
</dt> </dl>

 

 




