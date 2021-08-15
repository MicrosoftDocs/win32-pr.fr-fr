---
description: Si cette stratégie système par ordinateur est définie sur 1, les correctifs ne peuvent pas être supprimés de l’ordinateur par un utilisateur ou un administrateur.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5531d5afd7fa98883a3e07dc7c47db625db9051fa223ea7cd6f70e4ceb5aee03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378567"
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

 

 



