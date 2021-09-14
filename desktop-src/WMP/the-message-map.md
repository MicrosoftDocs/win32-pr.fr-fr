---
title: La table des messages
description: La table des messages
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- plug-ins Lecteur Windows Media, table des messages
- plug-ins, table des messages
- plug-ins d’interface utilisateur, table des messages
- Plug-ins d’interface utilisateur, table des messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7fc04caf752383368ab6e51ae19c82e8c3515
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118558"
---
# <a name="the-message-map"></a>La table des messages

La fenêtre du plug-in répond à différents événements en appelant des méthodes qui sont mappées aux messages d’événements correspondants. L’Assistant fournit un mappage afin que OnPaint et OnEraseBackground soient appelés aux moments appropriés. Pour créer le bouton de **recherche** et répondre aux clics, la section de la table des messages est modifiée comme suit :


```C++
BEGIN_MSG_MAP(CPluginWindow)
    MESSAGE_HANDLER(WM_PAINT, OnPaint)
    MESSAGE_HANDLER(WM_ERASEBKGND, OnEraseBackground)
    MESSAGE_HANDLER(WM_CREATE, OnCreate)
    COMMAND_ID_HANDLER(IDC_SEARCH, OnSearch)
END_MSG_MAP()

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




