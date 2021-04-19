---
description: L’opérateur de concaténation + = joint les caractères à la fin de cette chaîne. L’opérateur accepte un autre objet CHString, un pointeur de caractère ou un caractère unique.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'CHString :: Operator + = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538685"
---
# <a name="chstringoperator"></a>CHString :: Operator + =

\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

L’opérateur de concaténation + = joint les caractères à la fin de cette chaîne. L’opérateur accepte un autre objet [**CHString**](chstring.md) , un pointeur de caractère ou un caractère unique.

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="string"></span><span id="STRING"></span>*chaîne*
</dt> <dd>

Chaîne [**CHString**](chstring.md) qui effectue la concaténation à cette chaîne.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*cascade*
</dt> <dd>

Caractère à concaténer à cette chaîne.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère **null** à concaténer à cette chaîne.

</dd> </dl>

## <a name="remarks"></a>Notes

Sachez que les exceptions de mémoire peuvent se produire chaque fois que vous utilisez cet opérateur de concaténation, car un nouveau stockage peut être alloué pour les caractères ajoutés à cet objet [**CHString**](chstring.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de **CHString :: Operator + =**:


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>ChString. h (inclure FwCommon. h)</dt> </dl>                                                    |
| Bibliothèque<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CHString**](chstring.md)
</dt> </dl>

 

