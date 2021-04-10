---
description: Convertit la chaîne source spécifiée en chaîne Unicode, à l’aide de la page de codes UTF-8 (Unicode Transformation Format) de 8 bits.
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: Fonction RtlUTF8ToUnicodeN (WDM. h)
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200937"
---
# <a name="rtlutf8tounicoden-function"></a>RtlUTF8ToUnicodeN fonction)

Convertit la chaîne source spécifiée en chaîne Unicode, à l’aide de la page de codes UTF-8 (Unicode Transformation Format) de 8 bits.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UnicodeStringDestination* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon allouée par l’appelant qui reçoit la chaîne traduite.

</dd> <dt>

*UnicodeStringMaxByteCount* \[ dans\]
</dt> <dd>

Nombre maximal d’octets à écrire dans *UnicodeStringDestination*. Si cette valeur provoque la troncation de la chaîne traduite, **RtlUTF8ToUnicodeN** retourne un état d’erreur.

</dd> <dt>

*UnicodeStringActualByteCount* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable allouée par l’appelant qui reçoit la longueur, en octets, de la chaîne traduite. Ce paramètre est facultatif et peut avoir la **valeur null**. Si la chaîne est tronquée, le nombre retourné compte le nombre de chaînes tronquées réel.

</dd> <dt>

*UTF8StringSource* \[ dans\]
</dt> <dd>

Pointeur vers la chaîne à traduire.

</dd> <dt>

*UTF8StringByteCount* \[ dans\]
</dt> <dd>

Taille, en octets, de la chaîne sur *UTF8StringSource*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**RtlUTF8ToUnicodeN** retourne l’une des valeurs NTSTATUS suivantes :



| Code de retour                                                                                                  | Description                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**État de \_ réussite**</dt> </dl>               | La chaîne a été convertie en Unicode.<br/>                                                                 |
| <dl> <dt>**ÉTAT \_ \_ non \_ mappé**</dt> </dl>     | Un caractère d’entrée non valide a été rencontré et remplacé. Cet État est considéré comme un état de réussite.<br/> |
| <dl> <dt>**paramètre d’état \_ non valide \_**</dt> </dl>    | Les deux pointeurs vers *UnicodeStringDestination* et *UnicodeStringActualByteCount* étaient **null**.<br/>       |
| <dl> <dt>**Paramètre d’état \_ non valide \_ \_ 4**</dt> </dl> | *UTF8StringSource* a la **valeur null**.<br/>                                                                 |
| <dl> <dt>**\_mémoire tampon d’état \_ trop \_ petite**</dt> </dl>    | *UnicodeStringDestination* a été tronqué.<br/>                                                            |



 

## <a name="remarks"></a>Notes

Bien que *UnicodeStringActualByteCount* soit facultatif et peut avoir la **valeur null**, les appelants doivent fournir un stockage pour celui-ci, car la longueur reçue peut être utilisée pour déterminer si la conversion a réussi.

Si la sortie est tronquée et qu’un caractère d’entrée non valide est rencontré, la fonction retourne une \_ erreur de mémoire tampon d’état \_ insuffisante \_ .

Si *UnicodeStringDestination* a la valeur **null** , la fonction retourne le nombre d’octets requis pour héberger la chaîne traduite sans aucune troncation dans *UnicodeStringActualByteCount*.

**RtlUTF8ToUnicodeN** ne modifie pas la chaîne source, sauf si les pointeurs *UnicodeStringDestination* et *UTF8StringSource* sont équivalents. La chaîne Unicode retournée n’est pas terminée par un caractère null.

Les appelants de **RtlUTF8ToUnicodeN** doivent être exécutés au niveau IRQL < Dispatch \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>WDM. h</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RtlUnicodeToUTF8N**](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




