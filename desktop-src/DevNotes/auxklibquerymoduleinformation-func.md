---
description: Récupère des informations sur l’ensemble de modules actuellement chargés pour le système.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Fonction AuxKlibQueryModuleInformation (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540354"
---
# <a name="auxklibquerymoduleinformation-function"></a>AuxKlibQueryModuleInformation fonction)

Récupère des informations sur l’ensemble de modules actuellement chargés pour le système.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*BufferSize* \[ in, out\]
</dt> <dd>

En entrée, taille de la mémoire tampon *QueryInfo* , en octets. Sur la sortie, reçoit la taille réelle requise. Étant donné que la liste des modules système peut changer entre les appels, cette valeur peut également changer entre les appels.

</dd> <dt>

*Éléments* \[ dans\]
</dt> <dd>

Taille, en octets, d’un élément de tableau. Cette taille détermine le format de la sortie.

</dd> <dt>

*QueryInfo* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit les informations du module. Ces informations sont retournées dans un tableau dont les éléments sont l’une des structures suivantes : [**\_ informations de \_ base \_ sur le module**](aux-module-basic-info-struct.md) ou [**\_ \_ \_ informations étendues du module**](aux-module-extended-info-struct.md)aux. La structure spécifique utilisée dépend de la taille de l’élément spécifié.

Si ce paramètre a la **valeur null**, la fonction retourne la taille de mémoire tampon requise.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est STATUs \_ successful.

Si la fonction échoue, la valeur de retour peut être l’un des codes d’État définis dans Ntstatus. h, qui est disponible dans le kit WDK.

## <a name="remarks"></a>Notes

Vous devez appeler la fonction [**AuxKlibInitialize**](auxklibinitialize-func.md) avant d’appeler cette fonction.

La bibliothèque d’objets qui implémente cette API peut être téléchargée à partir d' [ici](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|------------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Bibliothèque d’API auxiliaires Windows version 1,0 ou ultérieure<br/>                            |
| En-tête<br/>          | <dl> <dt>Aux \_ klib. h</dt> </dl>   |
| Bibliothèque<br/>         | <dl> <dt>Aux \_ klib. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AuxKlibInitialize**](auxklibinitialize-func.md)
</dt> <dt>

[**\_informations de \_ base du module aux \_**](aux-module-basic-info-struct.md)
</dt> <dt>

[**\_ \_ informations étendues du module aux \_**](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




