---
description: Si cette stratégie système par ordinateur est définie sur &\# 0034 ; 1&\# 0034 ;, le programme d’installation empêche les non-administrateurs d’utiliser la mise à jour corrective du contrôle de compte d’utilisateur (UAC) pour n’importe quelle application installée sur l’ordinateur.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821eb480ac09a2fc0416d7b3a54c0df5699a7096b45e56a843afe691886296f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637776"
---
# <a name="disableluapatching"></a>DisableLUAPatching

Si cette stratégie système par ordinateur est définie sur « 1 », le programme d’installation empêche les non-administrateurs d’utiliser la mise à [jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md) pour les applications installées sur l’ordinateur. Lorsque la stratégie système par ordinateur n’est pas définie ou définie sur 0, les non-administrateurs peuvent appliquer des correctifs utilisateur de moindre privilège aux applications qui sont activées pour la mise à jour corrective des comptes d’utilisateur de moindre privilège.

Utilisez la propriété [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) pour empêcher la mise à jour corrective des privilèges les plus faibles d’une application.

la stratégie DisableLUAPatching est disponible à partir de Windows Installer version 3,0.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



