---
title: Méthode InkDraw
description: CGuiPaper conserve également un \_ indicateur m bInking. InkStart lui affecte la valeur TRUE pour signaler qu’une séquence de dessin est en cours. Par exemple, la méthode InkDraw utilise cet indicateur pour déterminer si elle doit peindre et enregistrer des données manuscrites.
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- InkDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e146093d23fd16d122da1ea81d1c99bdf06ed926d5cb4dba2f1d77b747b2058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662759"
---
# <a name="inkdraw-method"></a>Méthode InkDraw

CGuiPaper conserve également un \_ indicateur m bInking. [InkStart](inkstart-method.md) lui affecte la **valeur true** pour signaler qu’une séquence de dessin est en cours. Par exemple, la méthode InkDraw utilise cet indicateur pour déterminer si elle doit peindre et enregistrer des données manuscrites.

Voici la méthode InkDraw de GUIPAPER. Cotisations.


```C++
HRESULT CGuiPaper::InkDraw(
                       SHORT nX,
                       SHORT nY)
  {
    if (m_bInking)
    {
      // Start this ink line at previous old position.
      MoveToEx(m_hDC, m_OldPos.x, m_OldPos.y, NULL);

      // Assign new old position and draw the new line.
      LineTo(m_hDC, m_OldPos.x = nX, m_OldPos.y = nY);

      // Ask the Paper object to save this data.
      if (m_bInkSaving)
        m_pIPaper->InkDraw(m_nLockKey, nX, nY);
    }

    return NOERROR;
  }
```



Cette méthode ne fait rien si m \_ bInking a la **valeur false**. Il s’agit de la condition lorsque l’utilisateur déplace simplement la souris sur la fenêtre du client sans appuyer sur le bouton gauche de la souris.

InkDraw a clairement une responsabilité double. Les appels MoveToEx et LineTo Win32 sont effectués pour dessiner des images de ligne sur l’écran GUI (à l’aide du handle de contexte de périphérique conservé dans m \_ HDC). Les données d’entrée manuscrite sont également transmises à l’objet du colivre pour l’enregistrement à l’aide de la méthode InkDraw de l’interface [IPaper](ipaper-methods.md) . Quand m \_ bInkSaving a la **valeur false**, InkDraw peint l’image de ligne, mais ne stocke pas les données dans le codocument. Cette condition est utilisée lors du redessin.

 

 




