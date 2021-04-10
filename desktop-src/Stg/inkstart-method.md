---
title: Méthode InkStart
description: Les méthodes InkStart, InkDraw et InkStop utilisent toutes des constructions d’interface utilisateur graphique Win32, telles que les contextes de périphérique et les objets Pen.
ms.assetid: a639e1d2-6d81-472b-b639-d237e202020f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e25d02c4490106180298b6977ec539bd96fd03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940201"
---
# <a name="inkstart-method"></a>Méthode InkStart

Les méthodes **InkStart**, [**InkDraw**](inkdraw-method.md)et [**InkStop**](cguipaper-methods.md) utilisent toutes des constructions d’interface utilisateur graphique Win32, telles que les contextes de périphérique et les objets Pen. Cela illustre la raison pour laquelle CGuiPaper est nécessaire en tant que niveau distinct d’encapsulation. Les aspects de l’interface graphique utilisateur du papier de dessin sont gérés dans CGuiPaper. L’objet du colivre n’est envoyé que des données manuscrites.

Une autre raison de conception du niveau CGuiPaper d’encapsulation est la double nature de ses méthodes **InkStart**, [**InkDraw**](inkdraw-method.md)et [**InkStop**](cguipaper-methods.md) . Ils n’appellent pas seulement sur le conpapier pour enregistrer les données manuscrites lorsqu’elles se produisent. elles dessinent également une image visuelle du dessin tel qu’il se produit. CGuiPaper garde un \_ indicateur m bInkSaving pour gérer cette double nature. Lorsque m \_ bInkSaving a la valeur false, l’image est dessinée à l’écran, mais les données ne sont pas envoyées au codocument pour l’enregistrement.

Ce schéma est utilisé à des fins de redessiner lorsque l’utilisateur ne déplace pas la souris, mais que les données d’encre du copapier sont renvoyées à CGuiPaper pour un redessin automatique. CGuiPaper peut être invité à définir l' \_ indicateur m bInkSaving en appelant sa méthode [**InkSaving**](cguipaper-methods.md) .

Les exemples d’extraits de code suivants illustrent les méthodes **InkStart** de GUIPAPER. CPP ET RÉCEPTEUR. Cotisations.

## <a name="inkstart-method-guipapercpp"></a>Méthode InkStart (GUIPAPER. COTISATIONS


```C++
HRESULT CGuiPaper::InkStart(
                       SHORT nX,
                       SHORT nY)
  {
    HRESULT hr = E_FAIL;

    if (m_nLockKey || (!m_nLockKey && !m_bInkSaving))
    {
      // Start an ink drawing sequence only if one is not in progress.
      if (!m_bInking)
      {
        // Remember start position.
        m_OldPos.x = nX;
        m_OldPos.y = nY;

        // Delete old pen.
        if (m_hPen)
          DeleteObject(m_hPen);

        // Create and select the new drawing pen.
        m_hPen = CreatePen(PS_SOLID, m_nInkWidth, m_crInkColor);
        SelectObject(m_hDC, m_hPen);

        hr = NOERROR;

        // Ask the Paper object to mark the start of the ink drawing
        // sequence in the current ink color.
        if (m_pIPaper && m_bInkSaving)
        {
          hr = m_pIPaper->InkStart(
                            m_nLockKey,
                            nX,
                            nY,
                            m_nInkWidth,
                            m_crInkColor);
          // Capture the Mouse.
          SetCapture(m_hWnd);

          // We've modified the ink data--it is now "dirty" with
          // respect to the compound file image. Set dirty flag.
          m_bDirty = TRUE;
        }

        // Set inking flag to TRUE.
        m_bInking = TRUE;
      }
    }

    return hr;
  }
```



## <a name="inkstart-method-sinkcpp"></a>Méthode InkStart (SINK. COTISATIONS

**StoClien** reçoit les données de dessin sous la forme d’appels à l’interface **IPaperSink** connectée dans son objet COPaperSink. Ces méthodes correspondent aux méthodes **InkStart**, [**InkDraw**](inkdraw-method.md)et [**InkStop**](cguipaper-methods.md) similaires dans CGuiPaper.


```C++
STDMETHODIMP COPaperSink::CImpIPaperSink::InkStart(
                                              SHORT nX,
                                              SHORT nY,
                                              SHORT nWidth,
                                              COLORREF crInkColor)
  {
    // Turn off ink saving to the COPaper object.
    m_pBackObj->m_pGuiPaper->InkSaving(FALSE);

    // Play the data back to the CGuiPaper for display only.
    m_pBackObj->m_pGuiPaper->InkWidth(nWidth);
    m_pBackObj->m_pGuiPaper->InkColor(crInkColor);
    m_pBackObj->m_pGuiPaper->InkStart(nX, nY);

    return NOERROR;
  }
```



Quand **InkStart** est appelé dans le récepteur, il appelle CGuiPaper pour désactiver l’enregistrement manuscrit. Le délivreur n’a pas besoin de recevoir une copie en écho des données qu’il envoie. Quand [**InkDraw**](inkdraw-method.md) est appelé dans le récepteur, il passe simplement l’appel à **CGuiPaper :: InkDraw**. Quand [**InkStop**](cguipaper-methods.md) est appelé dans le récepteur, CGuiPaper est appelé pour réactiver l’enregistrement manuscrit. Le résultat est une lecture des données de l’encre du copapier vers CGuiPaper pour l’affichage uniquement.

Vous pouvez tester le comportement de **StoClien** lorsque son **IPaperSink** est déconnecté en choisissant l’option déconnecter dans le menu récepteur. En guise d’expérience, après avoir déconnecté le récepteur, choisissez à propos de dans le menu aide. La boîte de dialogue à propos de s’affiche, qui couvre une partie du dessin du **StoClien**. Cliquez sur OK dans la boîte de dialogue à propos de. Notez que la partie du dessin couverte est maintenant supprimée. Les données de dessin ne sont pas perdues, mais une partie de l’image est. Le client a reçu le \_ message de peinture WM et a émis la méthode [**IPaper :: Redraw**](ipaper--redraw.md) . Toutefois, étant donné que le récepteur n’était pas connecté, il n’a pas reçu les appels **IPaperSink** pour redessiner le dessin.

Vous pouvez également tester ce comportement en minimisant **StoClien** , puis en le restaurant. Dans ce cas, la totalité de l’image de dessin est perdue et doit être redessinée. Pour redessiner l’image de dessin après l’un de ces tests, utilisez le menu récepteur pour vous reconnecter, puis choisissez [**redessiner**](ipaper--redraw.md) dans le menu dessin.

 

 




