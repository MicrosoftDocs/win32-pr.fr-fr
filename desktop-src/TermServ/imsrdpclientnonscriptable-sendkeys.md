---
title: IMsRdpClientNonScriptable SendKeys, méthode
description: Envoie une série de séquences de touches au contrôle. Les séquences de touches sont sous forme de code d’analyse, c’est-à-dire les données de clavier des véritables clés physiques.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- SendKeys, méthode Services Bureau à distance
- SendKeys, méthode Services Bureau à distance, IMsRdpClientNonScriptable, interface
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable, méthode SendKeys
- SendKeys, méthode Services Bureau à distance, IMsRdpClientNonScriptable2, interface
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, méthode SendKeys
- SendKeys, méthode Services Bureau à distance, IMsRdpClientNonScriptable3, interface
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, méthode SendKeys
- SendKeys, méthode Services Bureau à distance, IMsRdpClientNonScriptable4, interface
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, méthode SendKeys
- SendKeys, méthode Services Bureau à distance, IMsRdpClientNonScriptable5, interface
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, méthode SendKeys
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466007"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a>IMsRdpClientNonScriptable :: SendKeys, méthode

Envoie une série de séquences de touches au contrôle. Les séquences de touches sont sous forme de code d’analyse, c’est-à-dire les données de clavier des véritables clés physiques.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*numKeys* \[ dans\]
</dt> <dd>

Nombre de séquences de touches à envoyer. Le nombre maximal de clés qui peuvent être envoyées en une seule opération est de 20. La méthode retourne **E \_ INVALIDARG** si ce paramètre est supérieur à 20. Pour plus d'informations, consultez la section Notes qui suit.

</dd> <dt>

*pbArrayKeyUp* \[ dans\]
</dt> <dd>

Tableau dont la taille est égale à *numKeys*. Un élément a la **valeur true** si la touche correspondante est active et **false** si la touche correspondante est enfoncée.

</dd> <dt>

*plKeyData* \[ dans\]
</dt> <dd>

Tableau dont la taille est égale à *numKeys*. Le tableau contient des données de séquence de touches et correspond à la valeur du paramètre *lParam* du message [WM \_](../inputdev/wm-keydown.md) KeyOut. Les données spécifient le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition. Pour obtenir une description des bits de ce tableau, consultez [WM \_ keydescendant](../inputdev/wm-keydown.md).

L’élément correspondant dans *pbArrayKeyUp* indique si la touche est vers le haut ou vers le haut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

La méthode **SendKeys** ne mélange pas les séquences de touches effectuées par l’utilisateur local avec les séquences de touches que la méthode envoie. Toutes les séquences de touches passées à la méthode sont envoyées à la session distante dans une seule séquence atomique.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                               |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable est défini en tant que 2f079c4c-87B2-4AFD-97ab-20cdb43038ae<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[WM- \_ touche](../inputdev/wm-keydown.md)
</dt> </dl>

 

