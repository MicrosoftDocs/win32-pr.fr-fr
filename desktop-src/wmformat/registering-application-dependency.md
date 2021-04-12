---
title: Inscription de la dépendance d’application (SDK Windows Media format 11)
description: Inscription de la dépendance d’application
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK, inscrire des dépendances d’application
- inscription des dépendances d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090cf61d32597800b52e2bc112d2bee1cc1b7cd7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032166"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a>Inscription de la dépendance d’application (SDK Windows Media format 11)

Les applications qui utilisent des API fournies par le kit de développement logiciel (SDK) Windows Media format ou le kit de développement logiciel (SDK) Windows Media Player dépendent des composants d’exécution de ces technologies. Vous pouvez inscrire votre application comme étant dépendante de ces composants dans le cadre de la configuration de votre application.

Lorsque vous inscrivez votre application, vous pouvez choisir l’un des deux niveaux de dépendance : blocage ou dépendant. Quand une ou plusieurs applications sont inscrites avec une dépendance de blocage sur l’un des composants d’exécution, le composant est bloqué d’une restauration vers une version antérieure. Les applications dépendantes qui ne sont pas inscrites comme bloquantes ne bloquent pas la restauration. Au lieu de cela, avant d’effectuer la restauration, l’utilisateur est invité à entrer un message indiquant que les applications sont dépendantes du composant.

Pour inscrire votre application, vous devez définir une valeur dans le Registre qui identifie votre application. La valeur de Registre à définir dépend du composant dont dépend votre application. Vous pouvez également définir deux valeurs supplémentaires par dépendance pour fournir des informations supplémentaires sur votre application.

Les valeurs de Registre suivantes sont utilisées pour inscrire la dépendance au runtime du SDK Windows Media Format :

-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ installation \\ *\_ type de référence* \\ application, «*application*»,*« \_ chaîne d’application*»
-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ - \\ *\_* \\ descripteur de type de référence, "*application*", "*\_ descripteur de référence*"
-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ installation \\ *\_ type de référence* \\ version,*application*, «*\_ version WMF*»

La valeur de Registre suivante est utilisée pour inscrire la dépendance au runtime du kit de développement logiciel (SDK) du lecteur Windows Media :

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

Version du lecteur Windows Media requise par votre application.

*\_version WMF*

Version du kit de développement logiciel (SDK) du format Windows Media requis par votre application.

Les trois exemples de valeurs de registre suivants montrent comment configurer les valeurs de votre application :

-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ Setup \\ DependentRefCounts \\ application, "southridgevideo", "Southridge Video Player"
-   HKEY \_ classes \_ racine \\ Software \\ Microsoft \\ windowsmedia \\ Setup \\ DependentRefCounts \\ Descriptor, "southridgevideo", "Southridge Video Player utilise le kit de développement logiciel (SDK) Windows Media format pour lire des fichiers vidéo."
-   HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ Setup \\ DependentRefCounts \\ version, "southridgevideo", "9.0.0.2600"

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Considérations relatives aux projets**](project-considerations.md)
</dt> </dl>

 

 




