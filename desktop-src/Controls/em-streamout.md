---
title: Message EM_STREAMOUT (RichEdit. h)
description: Fait en sorte qu’un contrôle RichEdit passe son contenu à une fonction de rappel EditStreamCallback définie par l’application \ 8211 ;. La fonction de rappel peut ensuite écrire le flux de données dans un fichier ou tout autre emplacement qu’il choisit.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- EM_STREAMOUT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942169"
---
# <a name="em_streamout-message"></a>\_Message STREAMOUT em

Fait en sorte qu’un contrôle RichEdit passe son contenu à une fonction de rappel [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) définie par l’application. La fonction de rappel peut ensuite écrire le flux de données dans un fichier ou tout autre emplacement qu’il choisit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le format de données et les options de remplacement.

Cette valeur doit être l’une des valeurs suivantes.



| Valeur                                                                                                                                                      | Signification                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**\_RTF SF**</dt> </dl>                   | RTF.<br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <dt>**\_RTFNOOBJS DF**</dt> </dl> | RTF avec espaces à la place des objets COM.<br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**\_texte SF**</dt> </dl>                | Texte avec des espaces à la place des objets COM.<br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <dt>**SF \_ texte**</dt> </dl>    | Texte avec une représentation textuelle des objets COM.<br/> |



 

L’option **DF \_ RTFNOOBJS** est utile si une application stocke des objets com lui-même, car la représentation RTF des objets com n’est pas très compacte. Le mot de contrôle \\ objattph, suivi d’un espace, indique la position de l’objet.

En outre, vous pouvez spécifier les indicateurs suivants.



| Valeur                                                                                                                                                            | Signification                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**\_PLAINRTF SFF**</dt> </dl>       | S’il est spécifié, le contrôle RichEdit diffuse uniquement les mots clés communs à tous les langages, en ignorant les mots clés spécifiques à une langue. S’il n’est pas spécifié, le contrôle RichEdit diffuse tous les mots clés. Vous pouvez combiner cet indicateur avec l’indicateur **DF \_ RTF** ou **DF \_ RTFNOOBJS** .<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**\_sélection SFF**</dt> </dl>    | S’il est spécifié, le contrôle RichEdit diffuse uniquement le contenu de la sélection actuelle. S’il n’est pas spécifié, le contrôle diffuse en continu le contenu entier. Vous pouvez combiner cet indicateur avec l’une des valeurs de format de données.<br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**\_Unicode DF**</dt> </dl>             | **Microsoft Rich Edit 2,0 et versions ultérieures :** Indique un texte Unicode. Vous pouvez combiner cet indicateur avec l’indicateur de **\_ texte DF** .<br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <dt>**DF \_ USECODEPAGE**</dt> </dl> | **Édition enrichie 3,0 et versions ultérieures :** Génère le format RTF UTF-8 ainsi que du texte à l’aide d’autres pages de codes. La page de codes est définie dans le mot de *wParam*. Par exemple, pour le format RTF UTF-8, affectez à *wParam* la valeur (CP \_ UTF8 << 16) \| SF \_ USECODEPAGE \| DF \_ RTF.<br/>                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . En entrée, le membre **pfnCallback** de cette structure doit pointer vers une fonction [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) définie par l’application. En sortie, le membre **dwError** peut contenir un code d’erreur différent de zéro si une erreur s’est produite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne le nombre de caractères écrits dans le flux de données.

## <a name="remarks"></a>Notes

Lorsque vous envoyez un **message \_ em STREAMOUT** , le contrôle RichEdit effectue des appels répétés à la fonction [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) spécifiée par le membre **pfnCallback** de la structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . À chaque fois qu’il appelle la fonction de rappel, le contrôle passe une mémoire tampon contenant une partie du contenu du contrôle. Ce processus se poursuit jusqu’à ce que le contrôle ait passé tout son contenu à la fonction de rappel, ou jusqu’à ce qu’une erreur se produise.

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

[**\_flux em**](em-streamin.md)
</dt> </dl>

 

 





