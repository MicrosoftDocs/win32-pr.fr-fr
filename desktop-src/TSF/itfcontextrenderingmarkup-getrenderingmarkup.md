---
title: Méthode ITfContextRenderingMarkup GetRenderingMarkup
description: La méthode ITfContextRenderingMarkup GetRenderingMarkup récupère un énumérateur des balises de rendu pour la plage donnée.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Infrastructure des services de texte de méthode GetRenderingMarkup
- GetRenderingMarkup méthode Text Services Framework, interface ITfContextRenderingMarkup
- ITfContextRenderingMarkup interface Text Services Framework, méthode GetRenderingMarkup
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a94c8a7cce8673560cf01091b819def343213bfde578df6ce1e8850e2721723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476952"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a>ITfContextRenderingMarkup :: GetRenderingMarkup, méthode

La méthode **ITfContextRenderingMarkup :: GetRenderingMarkup** récupère un énumérateur des balises de rendu pour la plage donnée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EC* \[ dans\]
</dt> <dd>

\[dans \] un cookie de modification en lecture seule pour accéder au contexte.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

\[in\]



| Valeur                                                                                                                                                                                         | Signification                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <dt>**\_ \_ propriété include GRM TF \_**</dt> </dl> | Si ce bit est 1, l’énumérateur inclut la propriété d' \_ attribut prop GUID \_ .<br/> |



 

</dd> <dt>

*pRangeCover* \[ dans\]
</dt> <dd>

\[dans \] un pointeur vers une interface [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) de la plage pour énumérer les balises de rendu.

</dd> <dt>

*ppEnum* \[ à\]
</dt> <dd>

\[\]un pointeur pour récupérer le pointeur d’interface [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                | Description                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Cette méthode n’est pas actuellement dans les fichiers d’en-tête publics. Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).

 

 

