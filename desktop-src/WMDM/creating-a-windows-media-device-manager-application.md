---
title: création d’une Application de Gestionnaire de périphériques multimédia Windows
description: création d’une Application de Gestionnaire de périphériques multimédia Windows
ms.assetid: 6a200bd9-19dd-4130-acb4-e038b469c334
keywords:
- Windows Gestionnaire de périphériques de média, création d’applications
- Gestionnaire de périphériques, création d’applications
- Windows Gestionnaire de périphériques de support, Guide de programmation
- Gestionnaire de périphériques, Guide de programmation
- Guide de programmation, applications de bureau
- guide de programmation, Windows Media Gestionnaire de périphériques
- Guide de programmation, plug-ins
- Guide de programmation, création d’applications
- Windows Gestionnaire de périphériques de média, applications de bureau
- Gestionnaire de périphériques, applications de bureau
- Windows Gestionnaire de périphériques de média, plug-ins
- Gestionnaire de périphériques, plug-INSP
- plug-ins, création
- plug-ins, Guide de programmation
- applications de bureau, création
- création d’applications Windows Media Gestionnaire de périphériques, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba468d4d9a04176847259087b8ba2626c2ffa3e0cac089f8433993320a7e125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585556"
---
# <a name="creating-a-windows-media-device-manager-application"></a>création d’une Application de Gestionnaire de périphériques multimédia Windows

cette section explique comment utiliser Windows Gestionnaire de périphériques Media dans votre application. Le terme « application » désigne ici un fichier exécutable, tel qu’un lecteur multimédia, ou un plug-in COM, tel qu’un plug-in de contrôle.

Microsoft inclut plusieurs fournisseurs de services avec Windows XP et Lecteur Windows Media 10, y compris un fournisseur de services MTP, un fournisseur de services de Windows CE (pour les appareils exécutant Windows CE et utilisant le protocole RAPI, tels que le Pocket PC) et un fournisseur de services pour les appareils de catégorie de stockage de masse (MSC). Vous pouvez également créer votre propre fournisseur de service pour garantir la communication avec votre propre appareil. Pour plus d’informations, consultez [création d’un fournisseur de services](creating-a-service-provider.md).

Il existe un certain nombre de fournisseurs de services hérités tiers qui concernent l’appareil non MTP, non-RAPI ou non-MTP d’un fabricant particulier. Ces fournisseurs de services sont inclus sur le disque de pilote fourni avec ces appareils.

une application qui utilise Windows Media Gestionnaire de périphériques doit effectuer les étapes suivantes.

1.  **Soyez conscient des problèmes de confidentialité liés au développement d’une application.** consultez la [déclaration de confidentialité](privacy-statement.md) pour en savoir plus sur certains problèmes de confidentialité impliquant le développement d’une application de Gestionnaire de périphériques multimédia Windows.
2.  **Incluez les fichiers d’en-tête et de bibliothèque requis pour votre application.** Consultez [fichiers d’en-tête et de bibliothèque requis pour une application](required-library-and-header-files-for-an-application.md) afin d’en savoir plus sur les fichiers que vous devez inclure dans votre projet.
3.  **Authentifiez l’application et obtenez l’interface IWMDMDevice racine.** la première tâche qu’une application doit effectuer pour utiliser Windows Media Gestionnaire de périphériques consiste à s’authentifier. ce processus vérifie l’identité de l’application pour Windows media Gestionnaire de périphériques à l’aide d’un certificat factice pour une fonctionnalité limitée de Gestionnaire de périphériques Windows media, ou à l’aide d’un certificat officiel pour des fonctionnalités complètes. Pour plus d’informations, consultez [authentification de l’application](authenticating-the-application.md).
4.  **Énumérer les appareils connectés.** la première étape de la communication avec les appareils consiste à déterminer quels appareils sont connectés et accessibles aux Gestionnaire de périphériques Windows Media. Pour plus d’informations, consultez [énumération des appareils](enumerating-devices.md).
5.  **Vérifiez l’état des composants DRM de l’appareil.** pour utiliser des fichiers protégés par drm, un appareil doit être créé sur une version de Windows Media drm pour les appareils mobiles, et les composants drm doivent être à jour. Avant de commencer à gérer des fichiers sur l’appareil, il est préférable de voir si l’appareil prend en charge les fichiers protégés par DRM et si l’appareil doit être mis à jour. Pour plus d’informations, consultez [gestion du contenu protégé dans l’application](handling-protected-content-in-the-application.md).
6.  **Explorez un appareil.** Une fois que vous avez trouvé l’appareil souhaité, vous pouvez explorer le contenu de cet appareil. Pour plus d’informations, consultez [exploration d’un appareil](exploring-a-device.md).
7.  **Lire des fichiers à partir de l’appareil et écrire des fichiers sur l’appareil.** Une fois que vous connaissez la disposition de l’appareil, vous pouvez commencer à transférer des fichiers vers et depuis l’appareil. Pour plus d’informations, consultez [lecture de fichiers à partir de l’appareil](reading-files-from-the-device.md) et [écriture de fichiers sur l’appareil](writing-files-to-the-device.md).
8.  **Créer des sélections sur l’appareil.** Un type de fichier que vous pouvez écrire sur l’appareil est un fichier abstrait, qui est une collection de références à d’autres fichiers. Bien que la possibilité d’écrire des fichiers abstraits sur un appareil dépende du fournisseur de services et de l’appareil, en général, seuls les appareils MTP disposent de cette fonctionnalité. Pour plus d’informations, consultez [création d’une sélection sur l’appareil](creating-a-playlist-on-the-device.md).

En plus de ces étapes, vous pouvez activer plusieurs autres fonctionnalités dans votre application :

-   Des **notifications.** Vous pouvez autoriser votre application à recevoir des notifications lorsque des appareils se connectent ou se déconnectent de l’ordinateur. Pour plus d’informations, consultez [activation des notifications](enabling-notifications.md).
-   **Journalisation.** Windows Le Gestionnaire de périphériques de média utilise un objet de journalisation qui enregistre un enregistrement de ses actions dans un fichier texte local. Vous pouvez ajouter des messages à ce journal pour vous aider à analyser les erreurs ou les performances de votre application. Pour plus d’informations, consultez Activation de la [journalisation](enabling-logging.md).
-   **Contrôle de l’utilisation du contenu.** Vous pouvez récupérer des statistiques d’utilisation de contenu pour les licences qui accordent ce droit. Ces statistiques peuvent ensuite être envoyées à un serveur Web pour calculer les paiements de droits d’accès aux propriétaires du contenu. Pour plus d’informations, consultez [contrôle de l’utilisation du contenu](metering-content-usage.md).

**Note de prudence**

Il se peut que votre application doive fonctionner avec un grand nombre d’appareils, y compris certains que vous n’avez pas développés et que vous n’avez jamais testé votre code. Ces appareils peuvent ou non répondre avec précision à des requêtes et des commandes, ou implémenter MTP ou d’autres spécifications. Veillez à inclure des fonctionnalités robustes de vérification des erreurs et de secours pour gérer les erreurs inattendues. Programmez de façon défensive.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 




