---
description: Implémente l’interface IInkDesktopHost.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: InkDesktopHost, classe
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: f422af645b3f5bc9431830c0ddab6f7321d09156b96fb6041104f684358bb9dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884586"
---
# <a name="inkdesktophost-class"></a>InkDesktopHost, classe

Implémente l’interface [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) .

Un objet [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) permet l’entrée d’encre, le traitement et le rendu via la création d’un thread d’application pour héberger un objet [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) et l’insérer dans l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) de l’application.

## <a name="members"></a>Membres

La classe **InkDesktopHost** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **InkDesktopHost** a également les types de membres suivants :

- [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **InkDesktopHost** possède ces méthodes.

| Méthode | Description |
|---|---|
| [**CreateAndInitializeInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | Crée un objet [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) sur un thread d’application, le connecte à l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) de l’application et définit la taille de l’objet.<br/> |
| [**CreateInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | Crée un objet [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) sur un thread d’application.<br/> |
| [**QueueWorkItem**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | Ajoutez une opération d’écriture manuscrite à une file d’attente de travail pour l’exécuter sur le thread **InkDesktopHost** .<br/> |

## <a name="creationaccess-functions"></a>Fonctions d’accès de création \\

Appelez [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec l’identificateur de classe <strong>InkDesktopHost</strong> pour récupérer une référence à l’objet.

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&_spInkHost));
```

## <a name="requirements"></a>Conditions requises

| Condition requise | Valeur |
|---|---|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/> |
| En-tête<br/>                   | <dl> <dt>InkPresenterDesktop. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>InkPresenterDesktop. idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkDesktopHost est défini en tant que 4ce7d875-A981-4140-a1ff-ad93258e8d59<br/> |

## <a name="related-topics"></a>Rubriques connexes

[Classes de présentateur d’encre](ink-presenter-classes.md), [interactions de stylet et](/windows/uwp/design/input/pen-and-stylus-interactions)de stylet, [exemple d’analyse](/samples/microsoft/windows-universal-samples/inkanalysis/)de l’encre, exemple d' [encrage simple](/samples/microsoft/windows-universal-samples/simpleink/), [exemple d’écriture](/samples/microsoft/windows-universal-samples/complexink/) manuscrite complexe
