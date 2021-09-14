---
description: Retourne un objet RecordList qui répertorie les produits qui utilisent un composant installé spécifié.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Installer. ClientsEx, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121685"
---
# <a name="installerclientsex-property"></a>Installer. ClientsEx, propriété

Cette propriété retourne un objet [**RecordList**](recordlist-object.md) qui répertorie les produits qui utilisent un composant installé spécifié. Cette propriété appelle [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. cette propriété est disponible à partir de Windows Installer 5,0.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.ClientsEx
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows programme d’installation 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




