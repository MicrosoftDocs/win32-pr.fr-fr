---
title: UtilAssembleStringsWithAlloc, fonction (Ndattributils. h)
description: Alloue une chaîne et la met en forme à l’aide de chaînes fournies par la table de chaînes. Cette fonction utilise StringCchPrintf pour créer la chaîne mise en forme.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- UtilAssembleStringsWithAlloc fonction NDF
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743884"
---
# <a name="utilassemblestringswithalloc-function"></a>UtilAssembleStringsWithAlloc fonction)

La fonction **UtilAssembleStringsWithAlloc** alloue une chaîne et la met en forme à l’aide de chaînes fournies par la table de chaînes. Cette fonction utilise [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) pour créer la chaîne mise en forme.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Mémoire tampon* \[ à\]
</dt> <dd>

Tapez : **LPWStr \** _

Emplacement où la chaîne qui vient d’être allouée sera placée. Lorsque la chaîne n’est plus nécessaire, elle doit être libérée avec [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*BufferMax* \[ dans\]
</dt> <dd>

Type : **uint**

Nombre maximal de caractères autorisés dans la chaîne allouée par *buffer*. Si la chaîne mise en forme obtenue est plus longue que le nombre de caractères spécifié, elle est tronquée et se termine par null.

> [!Note]  
> Ce paramètre ne peut pas être défini à zéro.

 

</dd> <dt>

*InputFormat* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Ressource de type chaîne de la table de chaînes représentant un paramètre de format passé à [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa). Il est construit à l’aide de [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

Le format de chaîne de ressource doit spécifier un paramètre de format acceptant une chaîne étendue, ou un paramètre de format qui accepte un entier long non signé et une chaîne étendue.

</dd> <dt>

*InputString* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Ressource de chaîne provenant de la table de chaînes qui représente un argument passé à [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) à la place de la chaîne étendue dans le paramètre de format. Il est construit à l’aide de [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

</dd> <dt>

*AdditionalArgument* \[ dans\]
</dt> <dd>

Type : **booléen**

True si *AdditionalValue* doit être passé en tant que premier argument de mise en forme à [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); Sinon, false (et seule la chaîne de ressource identifiée par *InputString* sera passée).

</dd> <dt>

*AdditionalValue* \[ dans\]
</dt> <dd>

Type : **ULong**

Valeur à passer comme premier argument de mise en forme à [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) si *AdditionalArgument* a la valeur true.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.



| Code de retour                                                                                  | Description                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | L’opération a réussi.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un ou plusieurs paramètres n’ont pas été fournis correctement.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> <dt>

[**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

