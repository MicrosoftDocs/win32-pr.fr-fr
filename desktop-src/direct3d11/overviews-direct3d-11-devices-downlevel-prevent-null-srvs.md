---
title: Prévention des SRVs de nuanceurs de pixels NULL indésirables
description: Cette rubrique explique comment contourner le pilote recevant des vues de nuanceur de ressource (SRVs) NULL, même lorsque les SRVs non NULL sont liés à l’étape nuanceur de pixels.
ms.assetid: c832c199-59b8-4079-a159-45490a2f6a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bacacf7704cffe12df44b9b0be667632307adb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990656"
---
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a><span data-ttu-id="e08e8-103">Prévention des SRVs de nuanceurs de pixels NULL indésirables</span><span class="sxs-lookup"><span data-stu-id="e08e8-103">Preventing Unwanted NULL Pixel Shader SRVs</span></span>

<span data-ttu-id="e08e8-104">Les applications Direct3D 11 qui s’exécutent sur le matériel graphique Direct3D 9 peuvent par inadvertance forcer le pilote à recevoir des vues de SRVs (Shader-Resource views) **null** , même lorsque les applications lient des SRVs non **null** à l’étape nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="e08e8-104">Direct3D 11 applications that run on Direct3D 9 graphics hardware could inadvertently cause the driver to receive **NULL** shader-resource views (SRVs) even when the applications bind non-**NULL** SRVs to the pixel shader stage.</span></span> <span data-ttu-id="e08e8-105">Cette situation peut se produire uniquement si les applications détruisent SRVs pendant leur exécution.</span><span class="sxs-lookup"><span data-stu-id="e08e8-105">This situation can occur only if the applications destroy SRVs while they execute.</span></span> <span data-ttu-id="e08e8-106">Cette rubrique explique comment contourner le pilote recevant des vues de nuanceur de ressource (SRVs) **null** , même lorsque les SRVs non **null** sont liés à l’étape nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="e08e8-106">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span>

<span data-ttu-id="e08e8-107">Pour empêcher le pilote de recevoir des SRVs **null** non souhaités, les applications doivent appeler [**ID3D11DeviceContext ::P ssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) pour annuler toutes les SRVs avant chaque appel à [**ID3D11DeviceContext ::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span><span class="sxs-lookup"><span data-stu-id="e08e8-107">To prevent the driver from receiving unwanted **NULL** SRVs, the applications must call [**ID3D11DeviceContext::PSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) to unset all SRVs before each call to [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span></span> <span data-ttu-id="e08e8-108">Toutefois, si les applications ne détruisent pas SRVs jusqu’à la fin de leur exécution de code, elles n’ont pas besoin d’annuler la SRVs.</span><span class="sxs-lookup"><span data-stu-id="e08e8-108">However, if the applications do not destroy SRVs until the end of their code execution, they do not need to unset the SRVs.</span></span>

<span data-ttu-id="e08e8-109">La section de [référence 10Level9](d3d11-graphics-reference-10level9.md) répertorie les différences entre la façon dont les différentes méthodes [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) et [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) se comportent à différents niveaux de fonctionnalités 10Level9.</span><span class="sxs-lookup"><span data-stu-id="e08e8-109">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e08e8-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e08e8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e08e8-111">Direct3D 11 sur du matériel de niveau inférieur</span><span class="sxs-lookup"><span data-stu-id="e08e8-111">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




