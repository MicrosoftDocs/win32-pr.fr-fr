---
title: Message EM_STREAMIN (RichEdit. h)
description: Remplace le contenu d’un contrôle RichEdit par un flux de données fourni par une application définie \ 8211 ; Fonction de rappel EditStreamCallback.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- EM_STREAMIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466347"
---
# <a name="em_streamin-message"></a>\_Message de flux em

Remplace le contenu d’un contrôle RichEdit par un flux de données fourni par une fonction de rappel [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) définie par l’application.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le format de données et les options de remplacement. Cette valeur doit être l’une des valeurs suivantes.



| Valeur                                                                                                                                       | Signification         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**\_RTF SF**</dt> </dl>    | RTF<br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**\_texte SF**</dt> </dl> | Texte<br/> |



 

En outre, vous pouvez spécifier les indicateurs suivants.



| Valeur                                                                                                                                                         | Signification                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**\_PLAINRTF SFF**</dt> </dl>    | S’il est spécifié, seuls les mots clés communs à tous les langages sont diffusés en continu. Les mots clés RTF spécifiques à une langue dans le flux sont ignorés. S’il n’est pas spécifié, tous les mots clés sont diffusés en continu. Vous pouvez combiner cet indicateur avec l’indicateur de **\_ format RTF SF** .<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**\_sélection SFF**</dt> </dl> | S’il est spécifié, le flux de données remplace le contenu de la sélection actuelle. S’il n’est pas spécifié, le flux de données remplace tout le contenu du contrôle. Vous pouvez combiner cet indicateur avec les indicateurs **\_ RTF** de **\_ texte** ou DF.<br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**\_Unicode DF**</dt> </dl>          | **Microsoft Rich Edit 2,0 et versions ultérieures :** Indique un texte Unicode. Vous pouvez combiner cet indicateur avec l’indicateur de **\_ texte DF** . <br/>                                                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . En entrée, le membre **pfnCallback** de cette structure doit pointer vers une fonction [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) définie par l’application. En sortie, le membre **dwError** peut contenir un code d’erreur différent de zéro si une erreur s’est produite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne le nombre de caractères lus.

## <a name="remarks"></a>Notes

Lorsque vous envoyez un message de **\_ flux em** , le contrôle RichEdit effectue des appels répétés à la fonction [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) spécifiée par le membre **pfnCallback** de la structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . Chaque fois que la fonction de rappel est appelée, elle remplit une mémoire tampon avec des données à lire dans le contrôle. Cela se poursuit jusqu’à ce que la fonction de rappel indique que l’opération de flux est terminée ou qu’une erreur se produit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**\_STREAMOUT em**](em-streamout.md)
</dt> </dl>

 

 





