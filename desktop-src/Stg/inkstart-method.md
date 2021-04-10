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
# <a name="inkstart-method"></a><span data-ttu-id="9704e-103">Méthode InkStart</span><span class="sxs-lookup"><span data-stu-id="9704e-103">InkStart Method</span></span>

<span data-ttu-id="9704e-104">Les méthodes **InkStart**, [**InkDraw**](inkdraw-method.md)et [**InkStop**](cguipaper-methods.md) utilisent toutes des constructions d’interface utilisateur graphique Win32, telles que les contextes de périphérique et les objets Pen.</span><span class="sxs-lookup"><span data-stu-id="9704e-104">**InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods all use Win32 GUI constructs such as device contexts and pen objects.</span></span> <span data-ttu-id="9704e-105">Cela illustre la raison pour laquelle CGuiPaper est nécessaire en tant que niveau distinct d’encapsulation.</span><span class="sxs-lookup"><span data-stu-id="9704e-105">This illustrates why CGuiPaper is needed as a separate level of encapsulation.</span></span> <span data-ttu-id="9704e-106">Les aspects de l’interface graphique utilisateur du papier de dessin sont gérés dans CGuiPaper.</span><span class="sxs-lookup"><span data-stu-id="9704e-106">The GUI aspects of the drawing paper are handled in CGuiPaper.</span></span> <span data-ttu-id="9704e-107">L’objet du colivre n’est envoyé que des données manuscrites.</span><span class="sxs-lookup"><span data-stu-id="9704e-107">The COPaper object is sent only ink data.</span></span>

<span data-ttu-id="9704e-108">Une autre raison de conception du niveau CGuiPaper d’encapsulation est la double nature de ses méthodes **InkStart**, [**InkDraw**](inkdraw-method.md)et [**InkStop**](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="9704e-108">Another design reason for the CGuiPaper level of encapsulation is the dual nature of its **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods.</span></span> <span data-ttu-id="9704e-109">Ils n’appellent pas seulement sur le conpapier pour enregistrer les données manuscrites lorsqu’elles se produisent. elles dessinent également une image visuelle du dessin tel qu’il se produit.</span><span class="sxs-lookup"><span data-stu-id="9704e-109">They not only call on COPaper to record the ink data as it occurs, they also paint a visual image of the drawing as it occurs.</span></span> <span data-ttu-id="9704e-110">CGuiPaper garde un \_ indicateur m bInkSaving pour gérer cette double nature.</span><span class="sxs-lookup"><span data-stu-id="9704e-110">CGuiPaper keeps an m\_bInkSaving flag to manage this dual nature.</span></span> <span data-ttu-id="9704e-111">Lorsque m \_ bInkSaving a la valeur false, l’image est dessinée à l’écran, mais les données ne sont pas envoyées au codocument pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9704e-111">When m\_bInkSaving is FALSE, the image is drawn on screen but the data is not sent to COPaper for recording.</span></span>

<span data-ttu-id="9704e-112">Ce schéma est utilisé à des fins de redessiner lorsque l’utilisateur ne déplace pas la souris, mais que les données d’encre du copapier sont renvoyées à CGuiPaper pour un redessin automatique.</span><span class="sxs-lookup"><span data-stu-id="9704e-112">This scheme is used in repainting when the user is not moving the mouse but COPaper's ink data is being resent to CGuiPaper for automatic repainting.</span></span> <span data-ttu-id="9704e-113">CGuiPaper peut être invité à définir l' \_ indicateur m bInkSaving en appelant sa méthode [**InkSaving**](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="9704e-113">CGuiPaper can be told to set the m\_bInkSaving flag by calling its [**InkSaving**](cguipaper-methods.md) method.</span></span>

<span data-ttu-id="9704e-114">Les exemples d’extraits de code suivants illustrent les méthodes **InkStart** de GUIPAPER. CPP ET RÉCEPTEUR. Cotisations.</span><span class="sxs-lookup"><span data-stu-id="9704e-114">The following sample code snippets illustrate the **InkStart** methods of GUIPAPER.CPP AND SINK.CPP.</span></span>

## <a name="inkstart-method-guipapercpp"></a><span data-ttu-id="9704e-115">Méthode InkStart (GUIPAPER. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="9704e-115">InkStart Method (GUIPAPER.CPP)</span></span>


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



## <a name="inkstart-method-sinkcpp"></a><span data-ttu-id="9704e-116">Méthode InkStart (SINK. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="9704e-116">InkStart Method (SINK.CPP)</span></span>

<span data-ttu-id="9704e-117">**StoClien** reçoit les données de dessin sous la forme d’appels à l’interface **IPaperSink** connectée dans son objet COPaperSink.</span><span class="sxs-lookup"><span data-stu-id="9704e-117">**StoClien** receives the drawing data in the form of calls to the connected **IPaperSink** interface in its COPaperSink object.</span></span> <span data-ttu-id="9704e-118">Ces méthodes correspondent aux méthodes **InkStart**, [**InkDraw**](inkdraw-method.md)et [**InkStop**](cguipaper-methods.md) similaires dans CGuiPaper.</span><span class="sxs-lookup"><span data-stu-id="9704e-118">These methods correspond to the similar **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods in CGuiPaper.</span></span>


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



<span data-ttu-id="9704e-119">Quand **InkStart** est appelé dans le récepteur, il appelle CGuiPaper pour désactiver l’enregistrement manuscrit.</span><span class="sxs-lookup"><span data-stu-id="9704e-119">When **InkStart** is called in the sink, it calls CGuiPaper to turn off ink saving to COPaper.</span></span> <span data-ttu-id="9704e-120">Le délivreur n’a pas besoin de recevoir une copie en écho des données qu’il envoie.</span><span class="sxs-lookup"><span data-stu-id="9704e-120">COPaper does not need to receive an echoed copy of the data it is sending.</span></span> <span data-ttu-id="9704e-121">Quand [**InkDraw**](inkdraw-method.md) est appelé dans le récepteur, il passe simplement l’appel à **CGuiPaper :: InkDraw**.</span><span class="sxs-lookup"><span data-stu-id="9704e-121">When [**InkDraw**](inkdraw-method.md) is called in the sink, it simply passes the call on to **CGuiPaper::InkDraw**.</span></span> <span data-ttu-id="9704e-122">Quand [**InkStop**](cguipaper-methods.md) est appelé dans le récepteur, CGuiPaper est appelé pour réactiver l’enregistrement manuscrit.</span><span class="sxs-lookup"><span data-stu-id="9704e-122">When [**InkStop**](cguipaper-methods.md) is called in the sink, CGuiPaper is called to turn ink saving back on.</span></span> <span data-ttu-id="9704e-123">Le résultat est une lecture des données de l’encre du copapier vers CGuiPaper pour l’affichage uniquement.</span><span class="sxs-lookup"><span data-stu-id="9704e-123">The result is a playback of COPaper's ink data to CGuiPaper for display only.</span></span>

<span data-ttu-id="9704e-124">Vous pouvez tester le comportement de **StoClien** lorsque son **IPaperSink** est déconnecté en choisissant l’option déconnecter dans le menu récepteur.</span><span class="sxs-lookup"><span data-stu-id="9704e-124">You can test the behavior of **StoClien** when its **IPaperSink** is disconnected by choosing the Disconnect choice on the Sink menu.</span></span> <span data-ttu-id="9704e-125">En guise d’expérience, après avoir déconnecté le récepteur, choisissez à propos de dans le menu aide.</span><span class="sxs-lookup"><span data-stu-id="9704e-125">As an experiment, after disconnecting the sink, choose About from the Help menu.</span></span> <span data-ttu-id="9704e-126">La boîte de dialogue à propos de s’affiche, qui couvre une partie du dessin du **StoClien**.</span><span class="sxs-lookup"><span data-stu-id="9704e-126">This will show the About dialog box, which will cover part of the **StoClien**'s drawing.</span></span> <span data-ttu-id="9704e-127">Cliquez sur OK dans la boîte de dialogue à propos de.</span><span class="sxs-lookup"><span data-stu-id="9704e-127">Click OK in the About dialog box.</span></span> <span data-ttu-id="9704e-128">Notez que la partie du dessin couverte est maintenant supprimée.</span><span class="sxs-lookup"><span data-stu-id="9704e-128">Notice that the portion of the drawing that was covered is now gone.</span></span> <span data-ttu-id="9704e-129">Les données de dessin ne sont pas perdues, mais une partie de l’image est.</span><span class="sxs-lookup"><span data-stu-id="9704e-129">The drawing data is not lost, but part of the image is.</span></span> <span data-ttu-id="9704e-130">Le client a reçu le \_ message de peinture WM et a émis la méthode [**IPaper :: Redraw**](ipaper--redraw.md) .</span><span class="sxs-lookup"><span data-stu-id="9704e-130">The client received the WM\_PAINT message and issued the [**IPaper::Redraw**](ipaper--redraw.md) method.</span></span> <span data-ttu-id="9704e-131">Toutefois, étant donné que le récepteur n’était pas connecté, il n’a pas reçu les appels **IPaperSink** pour redessiner le dessin.</span><span class="sxs-lookup"><span data-stu-id="9704e-131">But because the sink was not connected, it did not receive the **IPaperSink** calls to repaint the drawing.</span></span>

<span data-ttu-id="9704e-132">Vous pouvez également tester ce comportement en minimisant **StoClien** , puis en le restaurant.</span><span class="sxs-lookup"><span data-stu-id="9704e-132">You can also test this behavior by minimizing **StoClien** and then restoring it.</span></span> <span data-ttu-id="9704e-133">Dans ce cas, la totalité de l’image de dessin est perdue et doit être redessinée.</span><span class="sxs-lookup"><span data-stu-id="9704e-133">In this case, the entire drawing image is lost and needs repainting.</span></span> <span data-ttu-id="9704e-134">Pour redessiner l’image de dessin après l’un de ces tests, utilisez le menu récepteur pour vous reconnecter, puis choisissez [**redessiner**](ipaper--redraw.md) dans le menu dessin.</span><span class="sxs-lookup"><span data-stu-id="9704e-134">To repaint the drawing image after either of these tests, use the Sink menu to reconnect, and then choose [**Redraw**](ipaper--redraw.md) from the Draw menu.</span></span>

 

 




