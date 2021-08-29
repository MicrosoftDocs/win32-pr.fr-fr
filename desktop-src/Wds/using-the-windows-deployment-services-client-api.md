---
title: Utilisation de l’API du client des Services de déploiement Windows
description: dans les environnements où une solution standard Windows Deployment Services (WDS) ne peut pas être utilisée pour installer Windows, l’API du client WDS permet aux développeurs d’écrire des applications de déploiement personnalisées.
ms.assetid: abe2a7c7-989a-456e-80df-90d5b816db38
keywords:
- Windows services de déploiement Windows les services de déploiement, à l’aide de l’API client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6840f8327d1576a51d1f3d6cb7b097aaef87abc674bbbba0a004919ef5ce8366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760239"
---
# <a name="using-the-windows-deployment-services-client-api"></a>Utilisation de l’API du client des Services de déploiement Windows

dans les environnements où une solution standard Windows Deployment Services (WDS) ne peut pas être utilisée pour installer Windows, l’API du client WDS permet aux développeurs d’écrire des applications de déploiement personnalisées. Les applications peuvent utiliser cette API pour communiquer avec le serveur WDS pour obtenir des informations sur les images système disponibles sur le serveur. Les applications clientes WDS personnalisées doivent respecter les instructions suivantes.

## <a name="install-the-wds-role-on-the-server"></a>Installer le rôle WDS sur le serveur

-   Windows Services de déploiement (WDS) est la version révisée des services d’installation à distance (RIS), vous aurez besoin du rôle serveur WDS sur le serveur pour implémenter des solutions clientes WDS personnalisées.
-   WDS remplace RIS comme composant standard à partir de Windows server 2008 et Windows server 2003 avec Service Pack 2 (SP2).
-   vous devez mettre à jour le serveur RIS vers WDS sur Windows server 2003 avec Service Pack 1 (SP1). vous pouvez installer le rôle serveur WDS avec le [Kit d’installation automatisée (Windows AIK) (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="start-windows-pe-20"></a>démarrer Windows PE 2,0

Windows PE 2,0 doit être démarré, s’il n’est pas déjà démarré. le client WDS et les dll de prise en charge sont uniquement chargés par setup.exe lorsqu’il est dans la phase Microsoft environnement de préinstallation Windows (WinPE) (Windows PE 2,0) du traitement de l’installation.

-   Lorsqu’un nouvel ordinateur est connecté au réseau, vous pouvez utiliser la technologie de l’environnement d’exécution de prédémarrage (PXE) intégrée pour télécharger le programme de démarrage réseau. pour plus d’informations sur le démarrage PXE d’un ordinateur pour installer Windows, consultez [le Guide pas à pas de la mise à jour des Services de déploiement Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).
-   une image de démarrage RAMDISK de Windows PE 2,0 peut être stockée dans le. Format WIM et téléchargé dans le cadre du processus de démarrage réseau. Windows PE peut ensuite être chargé et exécuté directement à partir de ce média.

## <a name="open-a-session-with-the-wds-server"></a>Ouvrir une session avec le serveur WDS

Le client WDS doit ouvrir une session avec un serveur WDS.

-   Utilisez la fonction [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) pour ouvrir une session avec un serveur WDS. Cette fonction prend le nom ou l’adresse IP du serveur et reçoit l’adresse du descripteur pour la session du client WDS.
-   Si l’ouverture de la session avec le serveur nécessite l’authentification du client WDS, l’application doit fournir l’adresse d’une structure d’identification de la [**\_ CLI \_ WDS**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred) contenant les informations d’identification du client lors de l’appel de la fonction [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) . L’application peut utiliser la fonction [**WdsCliAuthorizeSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession) pour convertir une session anonyme en session authentifiée.
-   Lorsque la session ouverte avec la fonction [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) n’est plus nécessaire, l’application doit utiliser la fonction [**WdsCliClose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) pour fermer le handle et libérer les ressources détenues par la session.

## <a name="enumerate-system-images-on-the-wds-server"></a>Énumérer les images système sur le serveur WDS

Le client WDS peut utiliser l’API pour énumérer les images système sur le serveur WDS.

-   Utilisez la fonction [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) pour obtenir un descripteur de la première image et initialiser l’énumération des images sur le serveur WDS.
-   Utilisez la fonction [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) pour incrémenter l’énumération démarrée par la fonction [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) . La fonction **WdsCliFindNextImage** obtient le handle pour l’image suivante.
-   Utilisez la fonction [**WdsCliGetImageIndex**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex) pour obtenir l’index d’image de l’image actuelle. Cette valeur est valide uniquement jusqu’à ce que les fonctions [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) ou [**WdsCliClose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) soient réutilisées.
-   Utilisez la fonction [**WdsCliGetEnumerationFlags**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags) pour obtenir des indicateurs d’information sur le filtrage d’images.

## <a name="get-information-about-images"></a>Obtenir des informations sur les images

Le client WDS peut utiliser l’API pour obtenir des informations sur les images sur un serveur WDS. Les fonctions suivantes obtiennent des informations sur l’image actuelle. Étant donné que les fonctions [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) et [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) modifient la valeur de handle d’image actuelle, l’application doit stocker toutes les informations qu’elle obtient et devra à l’avenir avant d’appeler à nouveau les fonctions **WdsCliFindFirstImage** ou **WdsCliFindNextImage** .

-   Utilisez la fonction [**WdsCliGetImageArchitecture**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture) pour récupérer l’architecture de processeur de l’image actuelle.
-   Utilisez la fonction [**WdsCliGetImagePath**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath) pour récupérer le chemin d’accès relatif au fichier image qui contient l’image actuelle.
-   Utilisez la fonction [**WdsCliGetImageSize**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize) pour récupérer la taille de l’image.
-   Utilisez la fonction [**WdsCliGetImageVersion**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion) pour récupérer la version de l’image.
-   Utilisez la fonction [**WdsCliGetImageLanguage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage) pour récupérer la langue par défaut de l’image actuelle.
-   Utilisez la fonction [**WdsCliGetImageLanguages**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages) pour récupérer un tableau de langues prises en charge par l’image actuelle.
-   Utilisez [**WdsCliGetImageLastModifiedTime**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime) retourne l’heure de la dernière modification de l’image actuelle.
-   Utilisez la fonction [**WdsCliGetImageName**](/windows/win32/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename) pour récupérer le nom de l’image actuelle.
-   Utilisez la fonction [**WdsCliGetImageDescription**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription) pour récupérer la description de l’image actuelle.
-   Utilisez la fonction [**WdsCliGetImageGroup**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup) pour obtenir le nom du groupe d’images pour l’image actuelle.
-   Utilisez la fonction [**WdsCliGetImageHalName**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname) pour obtenir le nom de la couche d’abstraction matérielle (HAL) de l’image actuelle.

## <a name="log-wds-client-events"></a>Enregistrer les événements du client WDS

La fonctionnalité de journalisation de la bibliothèque cliente WDS permet d’envoyer les événements de progression de l’installation du client au serveur WDS.

-   Utilisez la fonction [**WdsCliInitializeLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog) pour initialiser le journal pour la session du client WDS.
-   Utilisez la fonction [**WdsCliLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclilog) pour écrire des messages d’événements dans le journal du serveur WDS.
-   sur Windows server 2008, le serveur WDS écrit les événements du client dans un journal des événements spécifique à l’application, qui est affichable via eventvwr.exe, ainsi que le journal des traces de débogage. sur Windows server 2003 avec la journalisation du débogage activée, le serveur WDS écrit les événements du client dans le fichier journal situé dans% windir% \\ tracing \\ wdsserver. log. La journalisation du client WDS doit être activée sur le serveur pour capturer ces événements.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos de l’API Windows Deployment Services](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Utilisation de l’API du serveur des Services de déploiement Windows](using-the-windows-deployment-services-server-api.md)
</dt> </dl>

 

 