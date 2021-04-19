---
title: Interface ISoftKbd (Softkbdc. h)
description: L’interface ISoftKbd est utilisée par les applications et les services de texte pour implémenter un clavier logiciel.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- ISoftKbd interface Text Services Framework
- ISoftKbd interface Text Services Framework, Description
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510726"
---
# <a name="isoftkbd-interface"></a>Interface ISoftKbd

L’interface **ISoftKbd** est utilisée par les applications et les services de texte pour implémenter un clavier logiciel.

## <a name="members"></a>Membres

L’interface **ISoftKbd** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ISoftKbd** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISoftKbd** possède ces méthodes.



| Méthode                                                                                        | Description                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**AdviseSoftKeyboardEventSink**](isoftkbd-advisesoftkeyboardeventsink.md)                   | Installe un récepteur d’événements de clavier logiciel pour gérer les notifications OnKeySelection à partir du clavier logiciel.<br/> |
| [**CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md) | Crée une disposition de clavier logiciel à partir de la ressource spécifiée.<br/>                                        |
| [**CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | Crée une disposition de clavier logiciel à partir du fichier XML spécifié.<br/>                                        |
| [**CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)                         | Crée une fenêtre de clavier temporaire.<br/>                                                                    |
| [**DestroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)                       | Détruit une fenêtre de clavier temporaire.<br/>                                                                   |
| [**EnumSoftKeyboard**](isoftkbd-enumsoftkeyboard.md)                                         | Énumère les claviers logiciels possibles qui prennent en charge le langage spécifié.<br/>                        |
| [**GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)                               | Récupère la couleur de clavier programmable correspondant au type de couleur fourni.<br/>                        |
| [**GetSoftKeyboardPosSize**](isoftkbd-getsoftkeyboardpossize.md)                             | Récupère la position de départ et la taille d’un clavier conditionnel.<br/>                                       |
| [**GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)                           | Récupère la police de texte utilisée par un clavier conditionnel.<br/>                                                   |
| [**GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)                           | Récupère le mode de type pour un clavier conditionnel.<br/>                                                       |
| [**Initialiser**](isoftkbd-initialize.md)                                                     | Initialise tous les champs nécessaires pour un clavier logiciel et génère des dispositions de clavier conditionnel standard.<br/> |
| [**SelectSoftKeyboard**](isoftkbd-selectsoftkeyboard.md)                                     | Sélectionne le clavier logiciel spécifié.<br/>                                                               |
| [**SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)                                 | Définit le texte de l’étiquette à partir de la disposition d’un clavier conditionnel.<br/>                                           |
| [**SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)           | Définit une combinaison d’étiquette et de texte utilisée pour décrire un clavier conditionnel.<br/>                             |
| [**SetSoftKeyboardColors**](isoftkbd-setsoftkeyboardcolors.md)                               | Définit la couleur du clavier logiciel correspondant au type de couleur fourni.<br/>                             |
| [**SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)                             | Définit la position de départ et la taille d’un clavier conditionnel.<br/>                                            |
| [**SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)                           | Définit la police de texte utilisée par un clavier conditionnel.<br/>                                                        |
| [**SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)                           | Définit le mode de type pour un clavier conditionnel.<br/>                                                            |
| [**ShowKeysForKeyScanMode**](isoftkbd-showkeysforkeyscanmode.md)                             | Affiche les clés utilisées pour le mode d’analyse de clé pour un clavier conditionnel.<br/>                                  |
| [**ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)                                         | Affiche un clavier conditionnel.<br/>                                                                          |
| [**UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)               | Supprime un récepteur d’événements de clavier logiciel.<br/>                                                                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



 

