---
title: Désactivation des fonctionnalités de Services Bureau à distance
description: Pour renforcer la sécurité, vous pouvez choisir de désactiver les fonctionnalités de Services Bureau à distance.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/01/2020
ms.locfileid: "103941547"
---
# <a name="disabling-remote-desktop-services-features"></a>Désactivation des fonctionnalités de Services Bureau à distance

Pour renforcer la sécurité, vous pouvez choisir de désactiver les fonctionnalités de Services Bureau à distance telles que la redirection du presse-papiers et la redirection de l’imprimante pour les clients qui se connectent aux serveurs Bureau à distance hôte de session (hôte de session Bureau à distance) à l’aide du contrôle ActiveX Bureau à distance.

**Pour désactiver les fonctionnalités de Services Bureau à distance**

1.  Modifiez le registre de l’ordinateur client et ajoutez les clés suivantes :

    -   **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Terminal Server \\ DisableClipboardRedirection**
    -   **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Terminal Server \\ DisableDriveRedirection**
    -   **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Terminal Server \\ DisablePrinterRedirection**

2.  Affectez la valeur **reg \_ DWORD** 1 à la valeur des deux clés.

 

 




