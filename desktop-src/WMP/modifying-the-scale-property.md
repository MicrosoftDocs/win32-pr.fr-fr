---
title: Modification de la propriété Scale
description: Modification de la propriété Scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Plug-ins du lecteur Windows Media, exemples de propriétés Echo
- plug-ins, exemples de propriétés d’écho
- plug-ins de traitement de signal numérique, exemples de propriétés Echo
- Plug-ins DSP, exemples de propriétés Echo
- Echo DSP, exemple de plug-in, propriété Scale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508974"
---
# <a name="modifying-the-scale-property"></a><span data-ttu-id="f7db9-108">Modification de la propriété Scale</span><span class="sxs-lookup"><span data-stu-id="f7db9-108">Modifying the Scale Property</span></span>

<span data-ttu-id="f7db9-109">L’implémentation de l’Assistant par défaut expose la propriété Scale.</span><span class="sxs-lookup"><span data-stu-id="f7db9-109">The default wizard implementation exposes the scale property.</span></span> <span data-ttu-id="f7db9-110">Vous pouvez modifier l’implémentation existante pour exposer la propriété Delay Time à la place.</span><span class="sxs-lookup"><span data-stu-id="f7db9-110">You can change the existing implementation to expose the delay time property instead.</span></span>

<span data-ttu-id="f7db9-111">Tout d’abord, utilisez l’exemple suivant pour modifier les prototypes de fonction pour les fonctions obtenir une \_ échelle et mettre \_ à l’échelle dans Echo. h.</span><span class="sxs-lookup"><span data-stu-id="f7db9-111">First, use the following example to change the function prototypes for get\_scale and put\_scale in Echo.h.</span></span> <span data-ttu-id="f7db9-112">Modifiez le nom des méthodes et les types de données des paramètres :</span><span class="sxs-lookup"><span data-stu-id="f7db9-112">Change the name of the methods and the data types for the parameters:</span></span>


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



<span data-ttu-id="f7db9-113">Ensuite, modifiez les implémentations des méthodes d’extraction d' \_ échelle et de mise \_ à l’échelle dans Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="f7db9-113">Next, change the implementations of the get\_scale and put\_scale methods in Echo.cpp.</span></span> <span data-ttu-id="f7db9-114">Faites en sorte que le code corresponde aux exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="f7db9-114">Make the code match the following examples:</span></span>


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



<span data-ttu-id="f7db9-115">L’exemple de code précédent modifie les noms des méthodes et les types de données des paramètres.</span><span class="sxs-lookup"><span data-stu-id="f7db9-115">The preceding example code changes the method names and the parameter data types.</span></span> <span data-ttu-id="f7db9-116">Le nom de la variable membre doit avoir été modifié précédemment.</span><span class="sxs-lookup"><span data-stu-id="f7db9-116">The member variable name should have been changed previously.</span></span> <span data-ttu-id="f7db9-117">N’oubliez pas de modifier les commentaires qui introduisent chaque méthode également.</span><span class="sxs-lookup"><span data-stu-id="f7db9-117">Remember to change the comments that introduce each method as well.</span></span>

<span data-ttu-id="f7db9-118">À présent, modifiez la définition de l’interface.</span><span class="sxs-lookup"><span data-stu-id="f7db9-118">Now, change the interface definition.</span></span> <span data-ttu-id="f7db9-119">Le code suivant remplace le code dans la déclaration de l’interface IEcho dans Echo. idl :</span><span class="sxs-lookup"><span data-stu-id="f7db9-119">The following code replaces the code in the IEcho interface declaration in Echo.idl:</span></span>


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a><span data-ttu-id="f7db9-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7db9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7db9-121">**Exemples de propriétés Echo**</span><span class="sxs-lookup"><span data-stu-id="f7db9-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




