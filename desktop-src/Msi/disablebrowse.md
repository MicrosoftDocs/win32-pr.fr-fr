---
description: La définition de la valeur de cette stratégie système par ordinateur sur &\# 0034 ; 1&\# 0034 ; empêche les utilisateurs non administratifs d’utiliser une boîte de dialogue Parcourir pour localiser les sources des applications gérées stockées sur le support, telles que les CD-ROM.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091534"
---
# <a name="disablebrowse"></a>DisableBrowse

La définition de la valeur de cette [stratégie système](system-policy.md) par ordinateur sur « 1 » empêche les utilisateurs non administratifs d’utiliser une [boîte de dialogue Parcourir](browse-dialog.md) pour localiser les sources des [*applications gérées*](m-gly.md) stockées sur le média, telles que les CD-ROM. La zone de liste déroulante « utiliser la fonctionnalité à partir de » pour l’entrée directe est verrouillée et l’option « Parcourir... » le bouton est désactivé. Pour plus d’informations sur la navigation source, consultez [résilience source](source-resiliency.md).

DisableBrowse remplace AllowLockdownBrowse et empêche la navigation même si AllowLockdownBrowse est défini.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="remarks"></a>Notes

Dans certains cas, avec DisableBrowse défini, un utilisateur non administratif peut toujours être en charge d’installer des applications gérées à partir de sources sur un support correctement étiqueté. La définition de la stratégie DisableBrowse désactive uniquement la possibilité d’accéder aux sources. Il peut être utilisé pour empêcher un utilisateur non administratif d’accéder à une nouvelle source lors d’une installation, d’une réinstallation ou d’une réparation à la demande. Si [AllowLockdownMedia](allowlockdownmedia.md) est défini, l’utilisateur non administratif peut toujours installer une application gérée à partir d’un média correctement étiqueté.

DisableBrowse empêche l’utilisateur non administratif d’accéder à un nouvel emplacement de support ou à tout autre emplacement source. Pour plus d’informations sur la sécurisation des sources multimédias des applications gérées, consultez [résilience source](source-resiliency.md).

Pour plus d’informations sur l’interaction de cette stratégie avec les sources d’installation, consultez [gestion des sources d’installation](managing-installation-sources.md).

 

 



