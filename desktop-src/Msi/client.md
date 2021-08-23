---
description: L’objet client représente une relation entre un composant et un produit client.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Objet client
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4308084bb1e5e081668bbe85dfb458f747fe34b25be0dd1858b5a7b7fae8a269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328379"
---
# <a name="client-object"></a>Objet client

L’objet client représente une relation entre un composant et un produit client.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. cet objet est disponible à partir de Windows Installer 5,0.

## <a name="members"></a>Membres

L’objet **client** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **client** a ces propriétés.



| Propriété                                                 | Description                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](client-componentcode.md)<br/> | Code du composant en question.<br/> |
| [**Contexte**](client-context.md)<br/>             | Contexte du produit.<br/>                      |
| [**ProductCode**](client-productcode.md)<br/>     | Produit client du composant en question.<br/> |
| [**UserSID**](client-usersid.md)<br/>             | SID de l’utilisateur du composant.<br/>                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Programme d’installation 5,0 ou version ultérieure.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IClient est défini en tant que 000C1098-0000-0000-C000-000000000046<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de l’interface d’automatisation](using-the-automation-interface.md)
</dt> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




