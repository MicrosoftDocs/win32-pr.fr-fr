---
title: Propriétés prédéfinies (msctf. h)
description: Les valeurs suivantes identifient les propriétés définies par TSF. Le format de données et le contenu de chaque type de propriété sont inclus.
ms.assetid: d88f2eba-4c98-4b32-96e1-cd019fe0f7ad
keywords:
- Propriétés prédéfinies Text Services Framework
topic_type:
- apiref
api_name:
- Predefined Properties
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807d1be5d1cc025971ad294fac825b89a4a0a519
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513811"
---
# <a name="predefined-properties"></a>Propriétés prédéfinies

Les valeurs suivantes identifient les propriétés définies par TSF. Le format de données et le contenu de chaque type de propriété sont inclus.

## <a name="properties"></a>Propriétés



| Propriété                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_attribut prop \_ GUID**       | Contient une valeur [**TfGuidAtom**](tfguidatom.md) qui représente le **GUID** de l’attribut d’affichage. [**ITfCategoryMgr :: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) est utilisé pour convertir cette valeur en **GUID**. Pour plus d’informations, consultez [utilisation des attributs d’affichage](using-display-attributes.md).                                                                                                                                                                                                                                                                                                                                                                             |
| **GUID \_ prop \_ TEXTOWNER**       | Contient une valeur [**TfGuidAtom**](tfguidatom.md) qui représente l’identificateur de classe ( **CLSID** ) du service de texte qui possède le texte. [**ITfCategoryMgr :: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) est utilisé pour convertir cette valeur en **CLSID**.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **GUID \_ prop \_ ID de langue**          | Contient une valeur **DWORD** qui contient l’identificateur de langue ( **LangID** ) du texte dans le mot de poids faible.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **lecture du GUID \_ prop \_**         | Contient le texte de lecture phonétique pour le texte couvert par la propriété. Cela peut être différent du texte réel. Les applications du Windows Store ne prennent pas en charge cette propriété.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_composition GUID prop \_**       | Contient une valeur booléenne différente de zéro si le texte fait partie d’une composition ou zéro dans le cas contraire. S’il s’agit \_ d’une propriété VT vide, il peut être supposé que le texte ne fait pas partie d’une composition.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **GUID \_ prop \_ MODEBIAS**        | Contient une valeur [**TfGuidAtom**](tfguidatom.md) qui représente le type de décalage de mode pris en charge. [**ITfCategoryMgr :: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) est utilisé pour convertir cette valeur en **GUID**. Il peut s’agir de l’une des [**valeurs de biais du mode**](mode-bias-values.md).                                                                                                                                                                                                                                                                                                                                                                                                  |
| **GUID \_ prop \_ amour mon lifeATTICE**       | Contient un pointeur vers un objet [**ITfLMLattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **\_remplacements du GUID prop \_ TKB \_** | **À compter de Windows 8 :** Contient une valeur **DWORD** définie par le clavier tactile. Cette propriété peut être utilisée par les contrôles d’édition et les applications sensibles à TSF pour identifier la nature du texte dans la plage de texte couverte par la propriété, par exemple, si le texte de la plage résulte de l’insertion d’une suggestion de texte ou d’une correction automatique. <br/> La nature du texte dans la plage de texte couverte par la propriété s’étend également au type des alternatives qui seraient retournées par l’interface [**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) pour cette plage de texte dans le document.<br/> Consultez les notes suivantes pour connaître les valeurs possibles de cette propriété.<br/> |



 

## <a name="remarks"></a>Notes

La propriété de **\_ \_ \_ remplacements GUID prop TKB** peut avoir l’une des valeurs suivantes.



| Nom                                     | Valeur      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_autres normes TKB \_                | 0x00000001 | Indique que le clavier tactile a généré une liste de mots alternatifs possibles pour le texte de la plage couverte par la propriété, et que ni la plage de texte, ni les autres ne sont une correction automatique ou une suggestion de texte.                                                                                                                                                                                                              |
| TKB \_ alternatives \_ pour la \_ Correction automatique     | 0x00000002 | Indique que le clavier tactile a généré un autre mot qui doit automatiquement remplacer le texte de la plage de texte couverte par la propriété.<br/> Le clavier tactile n’appliquera pas la correction automatique sans y être invité par le contrôle ou l’application d’édition. L’interface de reconversion ([**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion)) doit être utilisée pour appliquer la correction au texte du document.<br/> |
| \_alternatives TKB \_ pour la \_ prédiction         | 0x00000003 | Indique que la plage de texte couverte par la propriété est une suggestion de texte qui a été générée par le clavier tactile et insérée dans le document par l’utilisateur.<br/> D’autres prédictions supplémentaires peuvent également être stockées en tant que propriété dans le document.<br/>                                                                                                                                                                     |
| \_Correction automatique de remplacements TKB \_ \_ appliquée | 0x00000004 | Indique que la plage de texte couverte par la propriété est une correction automatique fournie par le clavier tactile et appliquée par le biais de l’interface [**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) .<br/> Cette valeur peut être utilisée par les contrôles d’édition ou les applications, avec des \_ alternatives TKB \_ pour \_ la correction automatique, afin d’empêcher l’application répétée d’une correction automatique.<br/>                                                                               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TfGuidAtom**](tfguidatom.md)
</dt> <dt>

[**ITfCategoryMgr :: GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[Utilisation des attributs d’affichage](using-display-attributes.md)
</dt> <dt>

[**Valeurs de décalage de mode**](mode-bias-values.md)
</dt> <dt>

[**ITfLMLattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice)
</dt> </dl>

 

 





