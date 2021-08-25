---
description: La fonction AttachPropertyInstanceEx mappe une propriété existante à un emplacement spécifique dans les données reconnues et modifie la valeur des données de propriété.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: AttachPropertyInstanceEx, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ec0b874d55d149c9d049b8c6b2cafd716fe82c66410e2d3e1550b397c366
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911279"
---
# <a name="attachpropertyinstanceex-function"></a>AttachPropertyInstanceEx fonction)

La fonction **AttachPropertyInstanceEx** mappe une propriété existante à un emplacement spécifique dans les données reconnues et modifie la valeur des données de propriété.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers le frame en cours d’analyse. Utilisez le descripteur passé à la DLL de l’analyseur dans le paramètre *hFrame* de la fonction [**AttachProperties**](attachproperties.md) .

</dd> <dt>

*hProperty* \[ dans\]
</dt> <dd>

Handle vers une structure [**PROPERTYINFO**](propertyinfo.md) qui définit la propriété. Lorsque vous implémentez la fonction d’exportation de [**Registre**](register-parser.md) , vous spécifiez la structure **PROPERTYINFO** qui définit la propriété.

</dd> <dt>

*Longueur* \[ dans\]
</dt> <dd>

Longueur des données pour cette instance de la propriété.

</dd> <dt>

*lpData* \[ dans\]
</dt> <dd>

Pointeur vers l’emplacement dans les données reconnues où se trouve la valeur de la propriété. Utilisez le pointeur passé à la DLL de l’analyseur dans le paramètre *lpProtocol* de la fonction [**AttachProperties**](attachproperties.md) .

</dd> <dt>

*LengthEx* \[ dans\]
</dt> <dd>

Longueur de la longueur des données étendues, en octets.

</dd> <dt>

*lpDataEx* \[ dans\]
</dt> <dd>

Pointeur vers les données étendues, qui est généralement une variable de pile qui contient les données d’extension.

</dd> <dt>

*HelpID* \[ dans\]
</dt> <dd>

Identificateur (de 0 à 2047) utilisé pour définir une aide contextuelle pour une propriété.

Le numéro *HelpID* est relatif au fichier d’aide associé à la [*base de données de propriétés de*](p.md)protocole.

</dd> <dt>

*IndentLevel* \[ dans\]
</dt> <dd>

Niveau de mise en retrait (de 0 à 15) utilisé pour afficher une propriété hiérarchiquement.

Moniteur réseau utilise les niveaux 0 à 9. Le niveau 15 est une valeur spéciale qui permet à l’analyseur d’attacher une propriété masquée qui n’est pas visible.

</dd> <dt>

*IFlags* \[ dans\]
</dt> <dd>

Valeur de champ de bits qui indique l’ordre des BITs dans une propriété. Les analyseurs précédents qui *définissent* le paramétrage de la valeur 0 ou 1 devraient *maintenant définir l'* erreur de l’IFLAG \_ . Définissez ce paramètre sur l’une des valeurs suivantes.



| Valeur                                                                                                                                                         | Signification                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**\_erreur IFLAG**</dt> </dl>       | Les données du frame comportent une erreur.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ échangé**</dt> </dl> | Au moment de l’attachement, le **mot** Byte n’est pas au format Intel.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ Unicode**</dt> </dl> | Au moment de l’attachement, la **chaîne** est Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Remarques

La fonction **AttachPropertyInstanceEx** est appelée pendant l’implémentation de la fonction d’exportation [**AttachProperties**](attachproperties.md) . Quand une propriété est attachée aux données à l’aide de AttachPropertyInstanceEx, Moniteur réseau crée une structure [**PROPERTYINST**](propertyinst.md) qui définit l’instance de la propriété jointe et une structure [**PROPERTYINSTEX**](propertyinstex.md) qui définit les données étendues.

Si **AttachPropertyInstanceEx** est appelée et qu’aucune donnée étendue n’est fournie, le paramètre *lpDataEx* est **null** ou le paramètre *LengthEx* est 0, l’appel **AttachPropertyInstanceEx** est fonctionnellement équivalent à un appel [**AttachPropertyInstance**](attachpropertyinstance.md) .

Pendant l’implémentation de [**AttachProperties**](attachproperties.md), appelez [**AttachPropertyInstance**](attachpropertyinstance.md) pour utiliser les données telles qu’elles existent dans la capture. Vous pouvez également appeler la fonction **AttachPropertyInstanceEx** pour modifier les données de propriété. Toutefois, il est recommandé d’utiliser les données telles qu’elles existent dans la capture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




