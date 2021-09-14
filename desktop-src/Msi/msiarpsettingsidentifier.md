---
description: La propriété MSIARPSETTINGSIDENTIFIER contient une liste délimitée par des points-virgules des emplacements du registre où l’application stocke les paramètres et les préférences d’un utilisateur.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Propriété MSIARPSETTINGSIDENTIFIER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230135"
---
# <a name="msiarpsettingsidentifier-property"></a>Propriété MSIARPSETTINGSIDENTIFIER

La propriété **MSIARPSETTINGSIDENTIFIER** contient une liste délimitée par des points-virgules des emplacements du registre où l’application stocke les paramètres et les préférences d’un utilisateur. Pendant une mise à niveau du système d’exploitation, le programme d’installation peut utiliser ces informations pour améliorer l’expérience des utilisateurs qui migrent des applications.

La valeur de la propriété **MSIARPSETTINGSIDENTIFIER** est un texte littéral qui contient la liste des emplacements du registre où l’application stocke ses paramètres. La valeur peut spécifier plusieurs emplacements de Registre possibles. Séparez plusieurs emplacements du Registre à l’aide de points-virgules. Les paramètres d’application sont généralement stockés dans les ruches de Registre **HKCU** ou **HKLM** sous la forme : *\\ \\ version* de l’application d’entreprise. L’exemple suivant est une valeur possible pour la propriété **MSIARPSETTINGSIDENTIFIER** .

*MyCompany \\ AppSuite \\ 1,0 ; MyCompany \\ App1 \\ 1,0 ; MyCompany \\ App2 \\ 1,0*

Cette propriété est facultative et peut être définie dans la table de [Propriétés](property-table.md) . Si cette propriété apparaît dans la table de propriétés, la valeur ne doit pas être définie sur **null**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 4,5 sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




