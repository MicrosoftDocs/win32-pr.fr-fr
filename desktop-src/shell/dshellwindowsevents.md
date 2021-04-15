---
description: Reçoit les événements d’inscription de la fenêtre IShellWindows.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Objet DShellWindowsEvents (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983015"
---
# <a name="dshellwindowsevents-object"></a>Objet DShellWindowsEvents

Reçoit les événements d’inscription de la fenêtre [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) .

## <a name="members"></a>Membres

L’objet **DShellWindowsEvents** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **DShellWindowsEvents** a ces méthodes.



| Méthode                                                           | Description                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [**WindowRegistered**](dshellwindowsevents-windowregistered.md) | Appelé lorsqu’une fenêtre est inscrite en tant que fenêtre d’interpréteur de commandes. <br/> |
| [**WindowRevoked**](dshellwindowsevents-windowrevoked.md)       | Appelé lorsque l’inscription d’une fenêtre d’interpréteur de commandes est révoquée. <br/> |



 

## <a name="remarks"></a>Notes

Utilisez **DShellWindowsEvents** pour surveiller le moment où une fenêtre d’interpréteur de commandes est inscrite ou révoquée. Pour plus d’informations, consultez [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Produit<br/> | Internet Explorer 5<br/>                                                                                           |
| En-tête<br/>  | <dl> <dt>Exdisp. h</dt> </dl>                                      |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (version 5.00.2014.0216 ou ultérieure)</dt> </dl> |
| IID<br/>     | IID \_ IShellWindows<br/>                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShellWindows**](shellwindows.md)
</dt> </dl>

 

 




