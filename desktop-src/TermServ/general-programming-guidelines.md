---
title: Instructions de programmation générales
description: Instructions pour le développement d’applications dans un environnement de Services Bureau à distance.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b0e83daa98f59390408fa43f5c5f83ff547e3d0cad665d29922f4244913361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353880"
---
# <a name="general-programming-guidelines"></a>Instructions de programmation générales

Les sections suivantes fournissent des recommandations générales pour le développement d’applications dans un environnement de Services Bureau à distance.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Couche de compatibilité des applications](application-compatibility-layer.md)
</dt> <dd>

Pour exécuter des applications héritées dans un environnement Services Bureau à distance, vous pouvez utiliser la couche de compatibilité des applications Services Bureau à distance.

</dd> <dt>

[Instructions pour les applications client/serveur](client-server-application-guidelines.md)
</dt> <dd>

Les applications client/serveur ne doivent pas supposer qu’une seule connexion d’ordinateur équivaut à une seule session utilisateur.

</dd> <dt>

[Surveillance des connexions et des déconnexions de session](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

Pour inscrire une application avec Services Bureau à distance, stockez le nom de l’application de serveur de canal virtuel dans le registre en ajoutant une sous-clé.

</dd> <dt>

[Instructions relatives au matériel périphérique](peripheral-hardware-guidelines.md)
</dt> <dd>

Si leur périphérique matériel n’est pas conçu pour fonctionner sur une session à distance, les fournisseurs doivent s’assurer que le logiciel du pilote de périphérique force la désactivation de la redirection de l’appareil à l’aide d’une stratégie système ou d’une stratégie de groupe.

</dd> <dt>

[Liaison au moment de l’exécution à Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

Votre application peut utiliser l’API Services Bureau à distance pour établir une liaison dynamique avec l' Wtsapi32.dll au moment de l’exécution. Pour ce faire, votre application doit appeler la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour charger Wtsapi32.dll.

</dd> </dl>

 

 