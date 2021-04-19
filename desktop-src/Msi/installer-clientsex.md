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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544101"
---
# <a name="installerclientsex-property"></a>Installer. ClientsEx, propriété

Cette propriété retourne un objet [**RecordList**](recordlist-object.md) qui répertorie les produits qui utilisent un composant installé spécifié. Cette propriété appelle [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. Cette propriété est disponible à partir de Windows Installer 5,0.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.ClientsEx
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




