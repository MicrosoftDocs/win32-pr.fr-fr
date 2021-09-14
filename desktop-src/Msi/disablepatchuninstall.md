---
description: Si cette stratégie système par ordinateur est définie sur 1, les correctifs ne peuvent pas être supprimés de l’ordinateur par un utilisateur ou un administrateur.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091502"
---
# <a name="disablepatchuninstall"></a>DisablePatchUninstall

Si cette [stratégie système](system-policy.md) par ordinateur est définie sur 1, les correctifs ne peuvent pas être supprimés de l’ordinateur par un utilisateur ou un administrateur. la Windows Installer peut toujours supprimer un correctif qui n’est plus applicable à un produit. Si cette stratégie n’est pas définie, un utilisateur peut supprimer un correctif de l’ordinateur uniquement si l’utilisateur dispose des privilèges nécessaires pour supprimer le correctif. Cela peut dépendre du fait que l’utilisateur est un administrateur, si les paramètres de stratégie [DisableMsi](disablemsi.md) et [AlwaysInstallElevated a](alwaysinstallelevated.md) sont définis et si le correctif a été installé dans un contexte par utilisateur géré, non géré par utilisateur ou par ordinateur.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



