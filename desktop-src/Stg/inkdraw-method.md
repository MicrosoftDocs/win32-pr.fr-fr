---
title: Méthode InkDraw
description: CGuiPaper conserve également un \_ indicateur m bInking. InkStart lui affecte la valeur TRUE pour signaler qu’une séquence de dessin est en cours. Par exemple, la méthode InkDraw utilise cet indicateur pour déterminer si elle doit peindre et enregistrer des données manuscrites.
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- InkDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41973d3f8560f25a81ac1deb782bada51b015239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380218"
---
# <a name="inkdraw-method"></a><span data-ttu-id="0c990-106">Méthode InkDraw</span><span class="sxs-lookup"><span data-stu-id="0c990-106">InkDraw Method</span></span>

<span data-ttu-id="0c990-107">CGuiPaper conserve également un \_ indicateur m bInking.</span><span class="sxs-lookup"><span data-stu-id="0c990-107">CGuiPaper also keeps an m\_bInking flag.</span></span> <span data-ttu-id="0c990-108">[InkStart](inkstart-method.md) lui affecte la **valeur true** pour signaler qu’une séquence de dessin est en cours.</span><span class="sxs-lookup"><span data-stu-id="0c990-108">[InkStart](inkstart-method.md) sets it to **TRUE** to signal that a drawing sequence is in process.</span></span> <span data-ttu-id="0c990-109">Par exemple, la méthode InkDraw utilise cet indicateur pour déterminer si elle doit peindre et enregistrer des données manuscrites.</span><span class="sxs-lookup"><span data-stu-id="0c990-109">For example, the InkDraw method uses this flag to determine whether it should paint and save ink data.</span></span>

<span data-ttu-id="0c990-110">Voici la méthode InkDraw de GUIPAPER. Cotisations.</span><span class="sxs-lookup"><span data-stu-id="0c990-110">The following is the InkDraw method from GUIPAPER.CPP.</span></span>


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



<span data-ttu-id="0c990-111">Cette méthode ne fait rien si m \_ bInking a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="0c990-111">This method does nothing if m\_bInking is **FALSE**.</span></span> <span data-ttu-id="0c990-112">Il s’agit de la condition lorsque l’utilisateur déplace simplement la souris sur la fenêtre du client sans appuyer sur le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="0c990-112">This is the condition when the user is simply moving the mouse over the client window without pressing the left mouse button.</span></span>

<span data-ttu-id="0c990-113">InkDraw a clairement une responsabilité double.</span><span class="sxs-lookup"><span data-stu-id="0c990-113">InkDraw clearly has a dual responsibility.</span></span> <span data-ttu-id="0c990-114">Les appels MoveToEx et LineTo Win32 sont effectués pour dessiner des images de ligne sur l’écran GUI (à l’aide du handle de contexte de périphérique conservé dans m \_ HDC).</span><span class="sxs-lookup"><span data-stu-id="0c990-114">The Win32 MoveToEx and LineTo calls are made to draw line images on the GUI screen (using the device context handle kept in m\_hDC).</span></span> <span data-ttu-id="0c990-115">Les données d’entrée manuscrite sont également transmises à l’objet du colivre pour l’enregistrement à l’aide de la méthode InkDraw de l’interface [IPaper](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="0c990-115">The ink data is also passed to the COPaper object for recording using the [IPaper](ipaper-methods.md) interface's InkDraw method.</span></span> <span data-ttu-id="0c990-116">Quand m \_ bInkSaving a la **valeur false**, InkDraw peint l’image de ligne, mais ne stocke pas les données dans le codocument.</span><span class="sxs-lookup"><span data-stu-id="0c990-116">When m\_bInkSaving is **FALSE**, InkDraw paints the line image but does not store the data in COPaper.</span></span> <span data-ttu-id="0c990-117">Cette condition est utilisée lors du redessin.</span><span class="sxs-lookup"><span data-stu-id="0c990-117">This condition is used during repainting.</span></span>

 

 




