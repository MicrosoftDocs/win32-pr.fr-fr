---
description: Analyse le texte pour identifier les mots et fournit les résultats à l’objet WordSink.
ms.assetid: 42bfc961-c095-4380-9b55-b58a0d9f2c00
title: 'IWordInfo :: BreakText, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: f6f71e92137490d56c93d9443506c2d7ffa2688a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033599"
---
# <a name="iwordinfobreaktext-method"></a>IWordInfo :: BreakText, méthode

\[Cette méthode est obsolète et n’est pas prise en charge sur Windows Vista.\]

Analyse le texte pour identifier les mots et fournit les résultats à l’objet [WordSink](/previous-versions//ms691570(v=vs.85)) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BreakText(
  [in] TEXT_SOURCE *pTextSource,
  [in] IWordSink   *pWordSink,
  [in] DWORD       fBreakMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTextSource* \[ dans\]
</dt> <dd>

Pointeur vers une structure [de \_ source de texte](/previous-versions//ms690919(v=vs.85)) qui contient le texte Unicode.

</dd> <dt>

*pWordSink* \[ dans\]
</dt> <dd>

Pointeur vers l’objet [WordSink](/previous-versions//ms691570(v=vs.85)) qui reçoit et gère les mots générés par cette méthode. Si ce paramètre a la **valeur null**, la méthode n’interrompt pas la chaîne en mots.

</dd> <dt>

*fBreakMode* \[ dans\]
</dt> <dd>

Mode arrêt. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                   | Signification                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="IWORDINFO_BREAKTEXTMODE_DICTFORM"></span><span id="iwordinfo_breaktextmode_dictform"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ DICTFORM**</dt> <dt>0x00000002</dt> </dl> | Word permet de couper la chaîne de texte et de passer la forme du dictionnaire des mots à l’objet **WordSink** .<br/> |
| <span id="IWORDINFO_BREAKTEXTMODE_SMARTSEL"></span><span id="iwordinfo_breaktextmode_smartsel"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ SMARTSEL**</dt> <dt>0x00000001</dt> </dl> | Word permet de couper la chaîne de texte et de transmettre les mots à l’objet **WordSink** .<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.



| Code de retour                                                                            | Description                                                                                             |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | L’opération a réussi. Il n’y a plus de texte disponible pour le remplissage de la mémoire tampon *pTextSource* .<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl> | Le paramètre *pTextSource* a la **valeur null**.<br/>                                                     |



 

## <a name="remarks"></a>Notes

Utilisez le membre **pfnFillTextBuffer** de la structure de la **\_ source de texte** pour réapprovisionner le texte source. Cette méthode doit gérer toutes les valeurs de retour de la fonction de rappel **pfnFillTextBuffer** . Si une erreur se produit, terminez le traitement du texte dans la mémoire tampon avant de gérer l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                  |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWordInfo**](iwordinfo.md)
</dt> <dt>

[SOURCE de texte \_](/previous-versions//ms690919(v=vs.85))
</dt> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
