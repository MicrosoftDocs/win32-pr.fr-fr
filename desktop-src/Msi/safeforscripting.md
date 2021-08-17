---
description: Si cette stratégie système par ordinateur est définie sur &\# 0034 ; 1&\# 0034 ;, le programme d’installation ne invite pas les utilisateurs lorsque les scripts d’une page Web utilisent l’interface d’automatisation du programme d’installation.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9a78bded284a687994075fdda1276122df2ab68716c4aaf759b4f5750aeb15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990149"
---
# <a name="safeforscripting"></a>SafeForScripting

Si cette [stratégie système](system-policy.md) par ordinateur est définie sur « 1 », le programme d’installation ne invite pas les utilisateurs lorsque les scripts d’une page Web utilisent l' [interface d’automatisation](automation-interface.md)du programme d’installation.

Avant de définir cette stratégie, vous devez déterminer si l’invite de l’utilisateur doit être précitée pour fournir un niveau de sécurité approprié à vos utilisateurs. Si cette stratégie n’est pas définie, lorsqu’un script hébergé par un navigateur Internet tente d’installer une application, le système avertit l’utilisateur et lui demande d’accepter ou de refuser l’installation. La définition de SafeForScripting supprime cet avertissement et peut permettre l’installation d’applications sur le système sans la connaissance de l’utilisateur. Cette stratégie peut être utile pour une entreprise qui utilise des outils basés sur le Web pour distribuer des programmes.

pour plus d’informations, consultez [instructions pour la création d’Installations sécurisées](guidelines-for-authoring-secure-installations.md) et de [Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md) et [téléchargement d’une Installation à partir d’Internet](downloading-an-installation-from-the-internet.md).

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

 

 



