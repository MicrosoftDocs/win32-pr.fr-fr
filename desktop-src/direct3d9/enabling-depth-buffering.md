---
description: 'Après avoir créé une mémoire tampon de profondeur, comme décrit dans création d’un tampon de profondeur (Direct3D 9), vous activez la mise en mémoire tampon de profondeur en appelant la méthode IDirect3DDevice9 :: SetRenderState.'
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Activation de la mise en mémoire tampon de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317546"
---
# <a name="enabling-depth-buffering-direct3d-9"></a><span data-ttu-id="0e29e-103">Activation de la mise en mémoire tampon de profondeur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0e29e-103">Enabling Depth Buffering (Direct3D 9)</span></span>

<span data-ttu-id="0e29e-104">Après avoir créé une mémoire tampon de profondeur, comme décrit dans [création d’un tampon de profondeur (Direct3D 9)](creating-a-depth-buffer.md), vous activez la mise en mémoire tampon de profondeur en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="0e29e-104">After you create a depth buffer, as described in [Creating a Depth Buffer (Direct3D 9)](creating-a-depth-buffer.md), you enable depth buffering by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="0e29e-105">Définissez l' \_ État de rendu D3DRS ZENABLE pour activer la mise en mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="0e29e-105">Set the D3DRS\_ZENABLE render state to enable depth-buffering.</span></span> <span data-ttu-id="0e29e-106">Utilisez le \_ membre D3DZB true du type énuméré [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) (ou **true**) pour activer la mise en mémoire tampon z, D3DZB \_ USEW pour activer la mise en mémoire tampon w ou D3DZB \_ false (ou **false**) pour désactiver la mise en mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="0e29e-106">Use the D3DZB\_TRUE member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type (or **TRUE**) to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE (or **FALSE**) to disable depth buffering.</span></span>

> [!Note]  
> <span data-ttu-id="0e29e-107">Pour utiliser la mise en mémoire tampon w, votre application doit définir une matrice de projection conforme même si elle n’utilise pas le pipeline de transformation Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0e29e-107">To use w-buffering, your application must set a compliant projection matrix even if it doesn't use the Direct3D transformation pipeline.</span></span> <span data-ttu-id="0e29e-108">Pour plus d’informations sur la façon de fournir une matrice de projection appropriée, consultez [une matrice de projection avec l’W-friendly](projection-transform.md)</span><span class="sxs-lookup"><span data-stu-id="0e29e-108">For information about providing an appropriate projection matrix, see [A W-Friendly Projection Matrix](projection-transform.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0e29e-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e29e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e29e-110">Mémoires tampons de profondeur</span><span class="sxs-lookup"><span data-stu-id="0e29e-110">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
