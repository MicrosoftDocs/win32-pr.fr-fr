---
description: Ces opérateurs d’indice définissent ou obtiennent l’élément à l’index spécifié. Ces opérateurs sont un substitut pratique des méthodes SetAt et GetAt.
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'CHStringArray :: Operator [] (ChStrArr. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 859cfe52535aea0fb43d6195648215431f80cff86f0525b9ef7c5247b6a831a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131771"
---
# <a name="chstringarrayoperator--"></a>CHStringArray ::, opérateur \[\]

\[La classe [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

Ces opérateurs d’indice définissent ou obtiennent l’élément à l’index spécifié. Ces opérateurs sont un substitut pratique des méthodes [**setat**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) et [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) .

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*
</dt> <dd>

Un index d’entiers supérieur ou égal à zéro et inférieur ou égal à la valeur retournée par [ **GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)

</dd> </dl>

## <a name="return-values"></a>Valeurs de retour

Les opérateurs d’indice retournent l’élément pointeur [**CHString**](chstring.md) actuellement à cet index.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser le premier opérateur, qui appelle des tableaux qui ne sont pas **const**, sur le côté droit (r-value) ou sur le côté gauche (valeur l) d’une instruction d’assignation. Le deuxième, qui appelle pour les tableaux **const** , peut être utilisé uniquement à droite.

La version de débogage de la bibliothèque déclare si l’indice (à gauche ou à droite d’une instruction d’assignation) est hors limites.

## <a name="examples"></a>Exemples

L’exemple de code suivant illustre l’utilisation de [**CHStringArray :: \[ \] Operator**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>ChStrArr. h (inclure FwCommon. h)</dt> </dl>                                                    |
| Bibliothèque<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CHStringArray :: Add**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

[**CHStringArray :: GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))
</dt> <dt>

[**CHStringArray :: SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))
</dt> </dl>

