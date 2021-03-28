---
description: Contient l’objet d’application du dossier.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Propriété Folder. application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484040"
---
# <a name="folderapplication-property"></a>Folder. application, propriété

Contient l’objet d’application du dossier.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
Application = Folder.Application
```



## <a name="property-value"></a>Valeur de la propriété

Référence d’objet à l’objet d’application.

## <a name="remarks"></a>Notes

La propriété d' **application** retourne l’objet Automation pris en charge par l’application qui contient le contrôle WebBrowser, si cet objet est accessible. Sinon, cette propriété retourne l’objet Automation du contrôle WebBrowser.

Utilisez cette propriété avec les commandes **Set** et **CreateObject** ou à l’aide de la commande **GetObject** pour créer et manipuler une instance de l’application Internet Explorer.

> [!Note]  
> Toutes les méthodes ne sont pas implémentées pour tous les dossiers. Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL). Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                 |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




