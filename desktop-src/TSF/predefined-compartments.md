---
title: Compartiments prédéfinis (Ctffunc. h)
description: Les valeurs suivantes identifient les compartiments implémentés par Text Services Framework.
ms.assetid: 65177979-ff91-4f62-8ba5-3c426b221b6c
keywords:
- Framework de services de texte de compartiments prédéfinis
topic_type:
- apiref
api_name:
- Predefined Compartments
api_location:
- Ctffunc.h
- Mstctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc684c4aee55c3c2e1807458ee261ad55156e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105391"
---
# <a name="predefined-compartments"></a>Compartiments prédéfinis

Les valeurs suivantes identifient les compartiments implémentés par Text Services Framework.

Les identificateurs de compartiment suivants sont définis dans Ctffunc. idl et Ctffunc. h.



| Indicateur                                     | Valeur  | Description                                                                                                                                                                                                                                                                               |
|------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID du compartiment de la \_ composante \_ \_ audio           | VT \_ | **Valeur DWORD** égale à zéro si l’audio de l’API Speech (SAPI) est désactivé ou différent de zéro si l’audio SAPI est activé. Ce compartiment est spécifique à un objet gestionnaire de threads.                                                                                                                               |
| \_CFGMENU de \_ reconnaissance vocale des compartiments GUID \_       | VT \_ | **Valeur DWORD** égale à zéro si le menu Configuration vocale n’est pas disponible ou différent de zéro si le menu Configuration vocale est disponible. Ce compartiment est spécifique à un objet gestionnaire de threads.                                                                                               |
| \_DICTATIONSTAT de \_ reconnaissance vocale des compartiments GUID \_ | VT \_ | Valeur **DWORD** qui contient zéro ou une combinaison d’une ou plusieurs des commandes [**tf \_ \_ activées**](speech-recognition-constants.md), de **commande tf \_ \_ activée**, de **\_ dictée TF \_ sur** ou **tf \_ \_ sur** les valeurs. Ce compartiment est spécifique à un objet gestionnaire de threads. |
| \_État de \_ \_ l’interface utilisateur parole des COMpartiments GUID \_    | VT \_ | Valeur **DWORD** qui contient zéro ou une combinaison d’une ou plusieurs des valeurs de l’info- [**\_ \_ bulle TF Show**](speech-recognition-constants.md) ou **tf \_ Disable \_** . Il s’agit d’un compartiment global.                                                                                   |



 

Les identificateurs de compartiment suivants sont définis dans MSCTF. IDL et MSCTF. H.



| Indicateur                                                    | Valeur  | Description                                                                                                                                                                                                                                                   |
|---------------------------------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_EMPTYCONTEXT de compartiment GUID \_                         | VT \_ | **Valeur DWORD** différente de zéro si le contexte est vide ou zéro dans le cas contraire. Ce compartiment est spécifique à un objet de contexte.                                                                                                                                      |
| OPENCLOSE de l' \_ \_ écriture manuscrite du compartiment GUID \_               | VT \_ | **Valeur DWORD** différente de zéro si la reconnaissance de l’écriture manuscrite est ouverte ou égale à zéro si la reconnaissance de l’écriture manuscrite est fermée. Ce compartiment est spécifique à un objet gestionnaire de threads.                                                                                 |
| \_clavier du compartiment GUID \_ \_ désactivé                   | VT \_ | **Valeur DWORD** différente de zéro si le clavier est désactivé ou zéro dans le cas contraire. Ce compartiment est spécifique à un objet de contexte.                                                                                                                                  |
| \_conversion du \_ INPUTMODE clavier des compartiments GUID \_ \_      | VT \_ | Valeur **DWORD** de la combinaison correcte des indicateurs [**tf \_ CONVERSIONMODE \_**](flags-for-conversion-mode.md) . Ce compartiment est spécifique à un objet gestionnaire de threads.                                                                                      |
| \_ \_ \_ phrase INPUTMODE clavier du compartiment GUID \_        | VT \_ | Valeur **DWORD** [**tf \_ SENTENCEMODE \_**](flags-for-conversion-mode.md). Ce compartiment est spécifique à un objet gestionnaire de threads.                                                                                                                        |
| \_ \_ OPENCLOSE clavier du compartiment GUID \_                  | VT \_ | **Valeur DWORD** différente de zéro si le clavier est ouvert ou zéro si le clavier est fermé. Ce compartiment est spécifique à un objet gestionnaire de threads.                                                                                                               |
| \_PERSISTMENUENABLED de compartiment GUID \_                   | VT \_ | **Valeur DWORD** différente de zéro pour faire en sorte que le service de texte vocal active l’élément de menu **enregistrer les données vocales** ou zéro pour le désactiver. Ce compartiment est spécifique à un objet du gestionnaire de documents.                                                                   |
| \_reconnaissance vocale des compartiments GUID \_ \_ désactivée                     | VT \_ | Valeur **DWORD** qui contient zéro ou une combinaison d’une ou de plusieurs des valeurs de commandes de désactivation [**tf \_ \_**](speech-recognition-constants.md), **tf \_ \_ Disable** ou **tf \_ \_ Disable** . Ce compartiment est spécifique à un objet gestionnaire de threads. |
| \_OPENCLOSE de \_ reconnaissance vocale des compartiments GUID \_                    | VT \_ | **Valeur DWORD** différente de zéro si l’entrée vocale est active ou égale à zéro si l’entrée vocale est inactive. Il s’agit d’un compartiment global.                                                                                                                                      |
| \_TIPUISTATUS de compartiment GUID \_                          | VT \_ | Pas utilisé pour l'instant.                                                                                                                                                                                                                                           |
| \_TRANSITORYEXTENSION de compartiment GUID \_                  | VT \_ | Valeur **DWORD** [**tf \_ TRANSITORYEXTENSION \_ None**](values-for-guid-compartment-transitoryextension.md), **tf \_ TRANSITORYEXTENSION \_ float** ou **tf \_ TRANSITORYEXTENSION \_ ATSELECTION**. Ce compartiment est spécifique à un objet du gestionnaire de documents.  |
| \_compartiment GUID \_ TRANSITORYEXTENSION \_ DOCUMENTMANAGER | VT \_ | Valeur IUnknown pour l’interface [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) qui fait référence au document transitoire de ce gestionnaire de documents. Ce compartiment est spécifique à un objet du gestionnaire de documents.                                                         |
| \_ \_ TRANSITORYEXTENSION parent du compartiment GUID \_          | VT \_ | Valeur IUnknown pour l’interface [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) qui fait référence au gestionnaire de document parent de ce document transitif. Ce compartiment est spécifique à un objet du gestionnaire de documents.                                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                                                                                          |
| En-tête<br/>                   | <dl> <dt>Ctffunc. h ; </dt> <dt>Mstctf. h</dt> </dl>     |
| MIDL<br/>                      | <dl> <dt>Ctffunc. idl ; </dt> <dt>Mstctf. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Constantes de reconnaissance vocale**](speech-recognition-constants.md)
</dt> </dl>

 

 





