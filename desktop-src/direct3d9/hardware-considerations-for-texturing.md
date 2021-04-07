---
description: Le matériel actuel n’implémente pas nécessairement toutes les fonctionnalités que l’interface Direct3D active. Votre application doit tester le matériel de l’utilisateur et ajuster ses stratégies de rendu en conséquence.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Considérations matérielles relatives à la texturation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845669"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a><span data-ttu-id="4f7c6-104">Considérations matérielles relatives à la texturation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4f7c6-104">Hardware Considerations for Texturing (Direct3D 9)</span></span>

<span data-ttu-id="4f7c6-105">Le matériel actuel n’implémente pas nécessairement toutes les fonctionnalités que l’interface Direct3D active.</span><span class="sxs-lookup"><span data-stu-id="4f7c6-105">Current hardware does not necessarily implement all the functionality that the Direct3D interface enables.</span></span> <span data-ttu-id="4f7c6-106">Votre application doit tester le matériel de l’utilisateur et ajuster ses stratégies de rendu en conséquence.</span><span class="sxs-lookup"><span data-stu-id="4f7c6-106">Your application must test user hardware and adjust its rendering strategies accordingly.</span></span>

<span data-ttu-id="4f7c6-107">De nombreuses cartes d’accélération 3D ne prennent pas en charge les valeurs itérées diffuses comme arguments pour les unités de fusion.</span><span class="sxs-lookup"><span data-stu-id="4f7c6-107">Many 3D accelerator cards do not support diffuse iterated values as arguments to blending units.</span></span> <span data-ttu-id="4f7c6-108">Toutefois, votre application peut introduire des données de couleur itérées lorsqu’elle effectue une fusion de texture.</span><span class="sxs-lookup"><span data-stu-id="4f7c6-108">However, your application can introduce iterated color data when it performs texture blending.</span></span>

<span data-ttu-id="4f7c6-109">Un matériel 3D peut ne pas avoir une étape de fusion associée à la première texture.</span><span class="sxs-lookup"><span data-stu-id="4f7c6-109">Some 3D hardware may not have a blending stage associated with the first texture.</span></span> <span data-ttu-id="4f7c6-110">Sur ces adaptateurs, votre application doit effectuer une fusion au cours des deuxième et troisième étapes de texture dans le jeu de textures actuelles.</span><span class="sxs-lookup"><span data-stu-id="4f7c6-110">On these adapters, your application must perform blending in the second and third texture stages in the set of current textures.</span></span>

<span data-ttu-id="4f7c6-111">En raison de limitations dans la plupart des configurations matérielles actuelles, peu d’adaptateurs d’affichage peuvent effectuer une interpolation mipmap trilinéaire via l’interface de fusion de plusieurs textures proposée par [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="4f7c6-111">Because of limitations in much of today's hardware, few display adapters can perform trilinear mipmap interpolation through the multiple texture blending interface offered by [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span> <span data-ttu-id="4f7c6-112">Votre application peut utiliser la fusion de texture multipasse pour obtenir les mêmes effets, ou se dégrader en \_ mode de filtre mipmap de point D3DTEXF, qui est largement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4f7c6-112">Your application can use multipass texture blending to achieve the same effects, or degrade to the D3DTEXF\_POINT mipmap filter mode, which is widely supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f7c6-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f7c6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f7c6-114">Textures Direct3D</span><span class="sxs-lookup"><span data-stu-id="4f7c6-114">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
