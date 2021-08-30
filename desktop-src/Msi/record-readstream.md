---
description: La méthode ReadStream de l’objet record lit un nombre spécifié d’octets à partir d’un champ d’enregistrement qui contient des données de flux.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Record. ReadStream, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 85f3cf97175b28750408d28a6e164f8aaa5fe71ec18bb89fff8e5c4583fb85cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041939"
---
# <a name="recordreadstream-method"></a>Record. ReadStream, méthode

La méthode **ReadStream** de l’objet [**Record**](record-object.md) lit un nombre spécifié d’octets à partir d’un champ d’enregistrement qui contient des données de flux.

## <a name="syntax"></a>Syntaxe


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*case* 
</dt> <dd>

Numéro de champ obligatoire de la valeur dans l’enregistrement, de base 1.

</dd> <dt>

*length* 
</dt> <dd>

Nombre d’octets requis pour lire à partir du flux.

</dd> <dt>

*format* 
</dt> <dd>

Interprétation et retour requis des octets de données.



| Nom du paramètre                                                                                                                                                                                                                                                                  | Signification                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <dt>**msiReadStreamInteger**</dt> <dt>0</dt> </dl> | Sous la forme d’un entier long, la longueur doit être comprise entre 1 et 4.<br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <dt>**msiReadStreamBytes**</dt> <dt>1</dt> </dl>         | Données sous forme de **BSTR**(un octet par caractère).<br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <dt>**msiReadStreamAnsi**</dt> <dt>2</dt> </dl>             | Octets ANSI traduits en **BSTR** Unicode.<br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <dt>**msiReadStreamDirect**</dt> <dt>3</dt> </dl>     | Paires d’octets qui sont retournées directement sous forme de **BSTR**.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une chaîne qui contient le nombre demandé d’octets lus à partir d’un champ d’enregistrement.

## <a name="remarks"></a>Remarques

La valeur retournée d’un champ inexistant est une valeur vide. Si le flux a moins d’octets que le nombre demandé, la chaîne retournée est raccourcie de manière appropriée.

Pour obtenir un exemple de cette méthode, consultez [copier le fichier ANSI dans un champ de base de données](copy-ansi-file-into-a-database-field.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




