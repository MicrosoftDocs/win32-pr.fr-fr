---
title: Classe Win32_RDSHCollection
description: Gère une collection d’hôtes de session Bureau à distance.
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Win32_RDSHCollection de la classe Services Bureau à distance
- Win32_RDSHCollection de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465550"
---
# <a name="win32_rdshcollection-class"></a>\_Classe RDSHCollection Win32

Gère une collection d’hôtes de session Bureau à distance.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RDSHCollection** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ RDSHCollection** possède ces méthodes.



| Méthode                                                                      | Description                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshcollection.md)           | Récupère une valeur de propriété entière d’un objet **Win32 \_ RDSHCollection** .<br/>                                                                                                                  |
| [**GetStringProperty**](getstringproperty-win32-rdshcollection.md)         | Récupère une valeur de propriété de type chaîne d’un objet **Win32 \_ RDSHCollection** .<br/>                                                                                                                    |
| [**KeyValueCompareAndSet**](win32-rdshcollection-keyvaluecompareandset.md) | Compare la clé spécifiée dans la collection avec un comparand ; Si elles correspondent, la nouvelle valeur est affectée à la clé. Si la clé n’existe pas, la méthode insère la clé dans la collection.<br/> |
| [**KeyValueDelete**](win32-rdshcollection-keyvaluedelete.md)               | Supprime la clé spécifiée (et la valeur associée) de la collection.<br/>                                                                                                                       |
| [**KeyValueGet**](win32-rdshcollection-keyvalueget.md)                     | Récupère la valeur associée à la clé spécifiée dans la collection.<br/>                                                                                                                    |
| [**SetInt32Property**](setint32property-win32-rdshcollection.md)           | Met à jour une valeur de propriété entière d’un objet **Win32 \_ RDSHCollection** .<br/>                                                                                                                    |
| [**SetStringProperty**](setstringproperty-win32-rdshcollection.md)         | Met à jour une valeur de propriété de type chaîne d’un objet **Win32 \_ RDSHCollection** .<br/>                                                                                                                      |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ RDSHCollection** a ces propriétés.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient et définit l’alias de la collection.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtient et définit la description de la collection.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le nom de la collection.

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

**Windows server 2012 R2 et Windows server 2012 :** Cette propriété n’est pas disponible avant Windows Server 2016.

Type de collection.

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Normal** (0)


</dt> <dd></dd> <dt>



 (2)


</dt> <dd>

Réservé

</dd> <dt>



 (3)


</dt> <dd>

Réservé

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**Autopersonation** (5)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fournisseur de services de gestion Bureau à distance](rdms-api-reference.md)
</dt> </dl>

 

