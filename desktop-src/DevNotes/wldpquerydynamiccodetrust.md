---
description: Récupère une valeur qui détermine si le code dynamique de la liste de révocation de certificats .NET en mémoire ou sur disque spécifié est approuvé par la stratégie Device Guard.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: WldpQueryDynamicCodeTrust, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 00b26c8d237a8c6d725751be064c7b82fc7a600c452598a590a747ba10ae56d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075723"
---
# <a name="wldpquerydynamiccodetrust-function"></a>WldpQueryDynamicCodeTrust fonction)

Récupère une valeur qui détermine si le code dynamique de la liste de révocation de certificats .NET en mémoire ou sur disque spécifié est approuvé par la stratégie Device Guard.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fileHandle* 
</dt> <dd>

Handle vers le fichier de code dynamique sur disque à vérifier. Si *fileHandle* n’a pas la **valeur null**, *BaseImage* doit avoir la **valeur null**.

</dd> <dt>

*baseImage* 
</dt> <dd>

Pointeur vers le fichier PE en mémoire à vérifier. Si *baseImage* n’a pas la **valeur null**, *FileHandle* doit avoir la **valeur null**.

</dd> <dt>

*ImageSize* 
</dt> <dd>

Lorsque *baseImage* est non **null**, indique la taille de la mémoire tampon vers laquelle pointe *baseImage* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne **S \_ OK** en cas de réussite ou un code d’échec dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




