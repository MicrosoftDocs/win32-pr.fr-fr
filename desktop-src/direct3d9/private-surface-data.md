---
description: Vous pouvez stocker n’importe quel type de données spécifiques à l’application à l’aide d’une surface. Par exemple, une surface représentant une carte dans un jeu peut contenir des informations sur le terrain.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Données de surface privée (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515333"
---
# <a name="private-surface-data-direct3d-9"></a><span data-ttu-id="2ed7f-104">Données de surface privée (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2ed7f-104">Private Surface Data (Direct3D 9)</span></span>

<span data-ttu-id="2ed7f-105">Vous pouvez stocker n’importe quel type de données spécifiques à l’application à l’aide d’une surface.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-105">You can store any kind of application-specific data with a surface.</span></span> <span data-ttu-id="2ed7f-106">Par exemple, une surface représentant une carte dans un jeu peut contenir des informations sur le terrain.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-106">For example, a surface representing a map in a game might contain information about terrain.</span></span>

<span data-ttu-id="2ed7f-107">Une surface peut avoir plusieurs mémoires tampons de données privées.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-107">A surface can have more than one private data buffer.</span></span> <span data-ttu-id="2ed7f-108">Chaque mémoire tampon est identifiée par un GUID que vous fournissez lors de l’attachement des données à l’aire de conception.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-108">Each buffer is identified by a GUID that you supply when attaching the data to the surface.</span></span>

<span data-ttu-id="2ed7f-109">Pour stocker des données de surface privée, utilisez SetPrivateData, en passant un pointeur vers la mémoire tampon source, la taille des données et un GUID défini par l’application pour les données.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-109">To store private surface data, use SetPrivateData, passing a pointer to the source buffer, the size of the data, and an application-defined GUID for the data.</span></span> <span data-ttu-id="2ed7f-110">Éventuellement, les données sources peuvent exister sous la forme d’un objet COM ; dans ce cas, vous transmettez un pointeur vers le pointeur d’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’objet et vous définissez l' \_ indicateur D3DSPD IUNKNOWNPOINTER.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-110">Optionally, the source data can exist in the form of a COM object; in this case, you pass a pointer to the object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface pointer and you set the D3DSPD\_IUNKNOWNPOINTER flag.</span></span>

<span data-ttu-id="2ed7f-111">SetPrivateData alloue une mémoire tampon interne pour les données et la copie.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-111">SetPrivateData allocates an internal buffer for the data and copies it.</span></span> <span data-ttu-id="2ed7f-112">Vous pouvez ensuite libérer en toute sécurité l’objet ou la mémoire tampon source.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-112">You can then safely free the source buffer or object.</span></span> <span data-ttu-id="2ed7f-113">La mémoire tampon interne ou la référence d’interface est libérée lorsque FreePrivateData est appelé.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-113">The internal buffer or interface reference is released when FreePrivateData is called.</span></span> <span data-ttu-id="2ed7f-114">Cela se produit automatiquement lorsque la surface est libérée.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-114">This happens automatically when the surface is freed.</span></span>

<span data-ttu-id="2ed7f-115">Pour récupérer des données privées pour une surface, vous devez allouer une mémoire tampon de la taille correcte, puis appeler la méthode GetPrivateData, en passant le GUID qui a été assigné aux données.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-115">To retrieve private data for a surface, you must allocate a buffer of the correct size and then call the GetPrivateData method, passing the GUID that was assigned to the data.</span></span> <span data-ttu-id="2ed7f-116">Vous êtes responsable de la libération de la mémoire dynamique que vous utilisez pour cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-116">You are responsible for freeing any dynamic memory you use for this buffer.</span></span> <span data-ttu-id="2ed7f-117">Si les données sont un objet COM, cette méthode récupère le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2ed7f-117">If the data is a COM object, this method retrieves the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="2ed7f-118">Si vous ne connaissez pas la taille de la mémoire tampon à allouer, appelez d’abord GetPrivateData avec zéro dans pSizeOfData.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-118">If you don't know how big a buffer to allocate, first call GetPrivateData with zero in pSizeOfData.</span></span> <span data-ttu-id="2ed7f-119">Si la méthode échoue avec D3DERR \_ MOREDATA, elle retourne le nombre d’octets nécessaires pour la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-119">If the method fails with D3DERR\_MOREDATA, it returns the necessary number of bytes for the buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ed7f-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ed7f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed7f-121">Surfaces Direct3D</span><span class="sxs-lookup"><span data-stu-id="2ed7f-121">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 
