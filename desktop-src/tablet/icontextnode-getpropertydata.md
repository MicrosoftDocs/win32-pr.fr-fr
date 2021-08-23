---
description: Récupère des données spécifiques à l’application ou d’autres données de propriété pour l’identificateur spécifié.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'IContextNode :: GetPropertyData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 89e7ab9fb5213b41d53695b516b95b47193e8d803b207efd09216c743085927e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660719"
---
# <a name="icontextnodegetpropertydata-method"></a>IContextNode :: GetPropertyData, méthode

Récupère des données spécifiques à l’application ou d’autres données de propriété pour l’identificateur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPropertyDataId* \[ dans\]
</dt> <dd>

Identificateur des données.

</dd> <dt>

*pulPropertyDataSize* \[ in, out\]
</dt> <dd>

Taille des données en octets. La valeur transmise n’est pas utilisée.

</dd> <dt>

*ppbPropertyData* \[ à\]
</dt> <dd>

Pointeur vers un tableau d’entiers non signés 8 bits qui contient les données de propriété.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppbPropertyData* lorsque vous n’avez plus besoin des informations.

 

En plus de récupérer des données spécifiques à l’application qui ont été ajoutées avec [**IContextNode :: AddPropertyData**](icontextnode-addpropertydata.md), cette méthode est utilisée pour récupérer les propriétés communes qui sont décrites par les constantes des [Propriétés du nœud de contexte](context-node-properties.md) .

Les propriétés de type chaîne sont les suivantes :

-   GUID \_ CNP \_ RECOGNIZEDSTRING
-   GUID \_ CNP \_ SHAPENAME
-   GUID \_ AHP \_ ANALYSISHINTNAME
-   GUID \_ AHP \_ PREFIXTEXT
-   GUID \_ AHP \_ SUFFIXTEXT
-   GUID \_ AHP \_ FACTOID

La valeur de retour est ** \* WCHAR*_. Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en **\* WCHAR*_ , sa longueur retournée est `(length of the string + 1) _ sizeof(WCHAR)` .

Les propriétés de type booléen sont les suivantes :

-   GUID \_ AHP \_ OVERRIDELANGUAGEID
-   GUID \_ AHP \_ COERCETOFACTOID
-   GUID \_ AHP \_ WORDMODE

La valeur de retour est de **type Variant \_ booléen**. Si vous effectuez un cast du \* paramètre *PpbPropertyData* en **Variant \_ \* bool** , sa longueur retournée est `sizeof(VARIANT_BOOL)` .

GUID \_ AHP \_ Guide est une propriété de type guide. La valeur de retour est ** \* InkAnalysisRecognitionGuide* _. Si vous effectuez un cast du \_ paramètre *PpbPropertyData* en **\* InkAnalysisRecognitionGuide** , sa longueur retournée est `sizeof(InkAnalysisRecognitionGuide)` .

Les propriétés de type entier sont les suivantes :

-   GUID \_ CNP \_ LINENUMBER
-   GUID \_ CNP \_ POINTSPERINCH
-   GUID \_ CNP \_ CONFIDENCELEVEL
-   \_confirmation CNP \_ GUID
-   GUID \_ CNP \_ MAXIMUMSTROKECOUNT
-   \_ \_ segmentation GUID CNP
-   GUID \_ CNP \_ ALIGNMENTLEVEL

La valeur de retour est ** \* long* _. Si vous effectuez un cast du \_ paramètre *PpbPropertyData* vers **\* long** , sa longueur retournée est `sizeof(LONG)` .

Métriques de ligne : les propriétés de type sont les suivantes :

-   GUID \_ CNP \_ ascendants
-   GUID \_ CNP les \_ descendants
-   \_ligne de \_ base GUID CNP
-   GUID \_ CNP- \_ média

La valeur de retour est ** \* long*_. Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en **\* long*_ sa longueur retournée, cela signifie que `sizeof(LONG)_4` les valeurs (x, y) des points de départ sont suivies des valeurs (x, y) des points de fin.

GUID \_ CNP \_ TEXTRECOGNIZERID est une propriété **GUID** . La valeur de retour est ** \* GUID* _. Si vous effectuez un cast du \_ paramètre *PpbPropertyData* en **\* GUID** , sa longueur retournée est `sizeof(GUID)` .

GUID \_ CNP \_ ROTATEDBOUNDINGBOX est une propriété de cadre englobant pivotée. La valeur de retour est ** \* long*_. Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en **\* long*_ sa longueur retournée, cela signifie que `sizeof(LONG)_8` les valeurs (x, y) des quatre coins de la zone sont retournées.

GUID \_ CNP \_ HOTPOINT est une propriété de point réactif. La valeur de retour est ** \* long*_. Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en **long \**_ sa longueur retournée est `sizeof(LONG)_2` , ce qui signifie les valeurs (x, y) pour le point.

GUID \_ AHP \_ liste de mots est une propriété de liste de mots. La valeur de retour est ** \* WCHAR*_. Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en **WCHAR \**_ , sa longueur retournée est `n _ sizeof(WCHAR)` , où `n` est la somme des longueurs de chaîne du nombre de chaînes de la liste plus 1 pour chaque caractère de fin **null** pour chaque chaîne.

## <a name="examples"></a>Exemples

Cet exemple montre une méthode qui accède à la propriété de nœud de contexte AlignmentLevel d’un type de nœud de contexte de paragraphe.


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

