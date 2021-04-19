---
description: Si cette stratégie système par ordinateur est définie sur &\# 0034 ; 1&\# 0034 ;, le programme d’installation empêche les non-administrateurs d’utiliser la mise à jour corrective du contrôle de compte d’utilisateur (UAC) pour n’importe quelle application installée sur l’ordinateur.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535080"
---
# <a name="disableluapatching"></a>DisableLUAPatching

Si cette stratégie système par ordinateur est définie sur « 1 », le programme d’installation empêche les non-administrateurs d’utiliser la mise à [jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md) pour les applications installées sur l’ordinateur. Lorsque la stratégie système par ordinateur n’est pas définie ou définie sur 0, les non-administrateurs peuvent appliquer des correctifs utilisateur de moindre privilège aux applications qui sont activées pour la mise à jour corrective des comptes d’utilisateur de moindre privilège.

Utilisez la propriété [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) pour empêcher la mise à jour corrective des privilèges les plus faibles d’une application.

La stratégie DisableLUAPatching est disponible à partir de Windows Installer version 3,0.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



