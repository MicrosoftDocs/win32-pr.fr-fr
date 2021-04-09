---
description: Traduit la chaîne Unicode spécifiée en une nouvelle chaîne de caractères, à l’aide de la page de codes UTF-8 (Unicode Transformation Format) de 8 bits.
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Fonction RtlUnicodeToUTF8N (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110434"
---
# <a name="rtlunicodetoutf8n-function"></a>RtlUnicodeToUTF8N fonction)

Traduit la chaîne Unicode spécifiée en une nouvelle chaîne de caractères, à l’aide de la page de codes UTF-8 (Unicode Transformation Format) de 8 bits.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UTF8StringDestination* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon allouée par l’appelant pour recevoir la chaîne traduite.

</dd> <dt>

*UTF8StringMaxByteCount* \[ dans\]
</dt> <dd>

Nombre maximal d’octets à écrire dans *UTF8StringDestination*. Si cette valeur provoque la troncation de la chaîne traduite, **RtlUnicodeToUTF8N** retourne un état d’erreur.

</dd> <dt>

*UTF8StringActualByteCount* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable allouée par l’appelant qui reçoit la longueur, en octets, de la chaîne traduite. Ce paramètre est facultatif et peut avoir la **valeur null**. Si la chaîne est tronquée, le nombre retourné compte le nombre de chaînes tronquées réel.

</dd> <dt>

*UnicodeStringSource* \[ dans\]
</dt> <dd>

Pointeur vers la chaîne source Unicode à traduire.

</dd> <dt>

* UnicodeStringByteCount * \[ dans\]
</dt> <dd>

Spécifie le nombre d’octets dans la chaîne source Unicode vers laquelle pointe le paramètre *UnicodeStringSource* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**RtlUnicodeToUTF8N** retourne l’une des valeurs NTSTATUS suivantes :



| Code de retour                                                                                                  | Description                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**État de \_ réussite**</dt> </dl>               | La chaîne Unicode a été convertie en UTF-8.<br/>                                                           |
| <dl> <dt>**ÉTAT \_ \_ non \_ mappé**</dt> </dl>     | Un caractère d’entrée non valide a été rencontré et remplacé. Cet État est considéré comme un état de réussite.<br/> |
| <dl> <dt>**paramètre d’état \_ non valide \_**</dt> </dl>    | Les deux pointeurs vers *UTF8StringDestination* et *UTF8StringActualByteCount* étaient **null**.<br/>              |
| <dl> <dt>**Paramètre d’état \_ non valide \_ \_ 4**</dt> </dl> | *UnicodeStringSource* a la **valeur null**.<br/>                                                              |
| <dl> <dt>**\_mémoire tampon d’état \_ trop \_ petite**</dt> </dl>    | *UTF8StringDestination* a été tronqué.<br/>                                                               |



 

## <a name="remarks"></a>Notes

Bien que *UTF8StringActualByteCount* soit facultatif et peut avoir la **valeur null**, les appelants doivent fournir un stockage pour celui-ci, car la longueur reçue peut être utilisée pour déterminer si la conversion a réussi. Cette routine ne modifie pas la chaîne source. Elle retourne une chaîne UTF-8 terminée par le caractère NULL si le *UnicodeStringSource* donné a inclus un terminateur null et si le *UTF8StringMaxByteCount* donné n’a pas provoqué la troncation.

Si la sortie est tronquée et qu’un caractère d’entrée non valide est rencontré, la fonction retourne une \_ erreur de mémoire tampon d’état \_ insuffisante \_ .

Si *UTF8StringDestination* a la valeur **null** , la fonction retourne le nombre d’octets requis pour héberger la chaîne traduite sans aucune troncation dans *UTF8StringActualByteCount*.

Les appelants de **RtlUnicodeToUTF8N** doivent être exécutés au niveau IRQL < Dispatch \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>WDM. h</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RtlUTF8ToUnicodeN**](rtlutf8tounicoden.md)
</dt> </dl>

 

 




