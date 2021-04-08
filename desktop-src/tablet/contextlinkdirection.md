---
description: Spécifie la direction d’un objet IContextLink.
ms.assetid: 4ba7dca7-6801-45bf-bbf1-1dd3172fbfa2
title: Énumération ContextLinkDirection (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContextLinkDirection
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 82e10c7e908b4cc4035d8bfdde55d863f7b6ecf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865829"
---
# <a name="contextlinkdirection-enumeration"></a><span data-ttu-id="93b4e-103">Énumération ContextLinkDirection</span><span class="sxs-lookup"><span data-stu-id="93b4e-103">ContextLinkDirection enumeration</span></span>

<span data-ttu-id="93b4e-104">Spécifie la direction d’un objet [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="93b4e-104">Specifies the direction of an [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="93b4e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93b4e-105">Syntax</span></span>


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a><span data-ttu-id="93b4e-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="93b4e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="93b4e-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection \_ LinksWith**</span><span class="sxs-lookup"><span data-stu-id="93b4e-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection\_LinksWith**</span></span>
</dt> <dd>

<span data-ttu-id="93b4e-108">Le [**IContextNode**](icontextnode.md) est un dessin directionnel qui pointe vers l’extérieur du [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="93b4e-108">The [**IContextNode**](icontextnode.md) is a directional drawing that points away from the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="93b4e-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection \_ LinksFrom**</span><span class="sxs-lookup"><span data-stu-id="93b4e-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection\_LinksFrom**</span></span>
</dt> <dd>

<span data-ttu-id="93b4e-110">Le [**IContextNode**](icontextnode.md) est un dessin directionnel qui pointe vers le [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="93b4e-110">The [**IContextNode**](icontextnode.md) is a directional drawing that points to the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="93b4e-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection \_ LinksTo**</span><span class="sxs-lookup"><span data-stu-id="93b4e-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection\_LinksTo**</span></span>
</dt> <dd>

<span data-ttu-id="93b4e-112">Il n’existe aucun dessin directionnel dans le lien.</span><span class="sxs-lookup"><span data-stu-id="93b4e-112">There are no directional drawings in the link.</span></span> <span data-ttu-id="93b4e-113">Par exemple, un dessin manuscrit peut souligner un mot manuscrit.</span><span class="sxs-lookup"><span data-stu-id="93b4e-113">For example, an ink drawing can underline an ink word.</span></span> <span data-ttu-id="93b4e-114">Aucune direction n’est déduite du soulignement.</span><span class="sxs-lookup"><span data-stu-id="93b4e-114">There is no direction inferred from the underline.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="93b4e-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="93b4e-115">Examples</span></span>

<span data-ttu-id="93b4e-116">L’exemple suivant prend un objet [**IContextNode**](icontextnode.md) , `m_pSelectedNode` , et enregistre tous les objets **IContextNode** auxquels il est lié en parcourant l’arborescence ancêtre et en ajoutant les objets dans un `CArray` objet `linkedToNodes` .</span><span class="sxs-lookup"><span data-stu-id="93b4e-116">The following example takes an [**IContextNode**](icontextnode.md) object, `m_pSelectedNode`, and saves all the **IContextNode** objects that it links to by walking up the ancestor tree and adding the objects into a `CArray` object, `linkedToNodes`.</span></span> <span data-ttu-id="93b4e-117">`CheckHResult` est une fonction qui accepte un `HRESULT` et une chaîne, et lève une exception créée avec la chaîne si le `HRESULT` n’a pas **réussi**.</span><span class="sxs-lookup"><span data-stu-id="93b4e-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
// Find all first ancestor that contains links of type Enclose
CArray<IContextNode*,IContextNode*> linkedToNodes = CArray<IContextNode*,IContextNode*>();
IContextNode* pAncestor;
CheckHResult(m_pSelectedNode->GetParentNode(&pAncestor),
    "IContextNode::GetParentNode failed");
while (pAncestor != NULL)
{
    // Get the links
    IContextLinks* pLinks;
    CheckHResult(pAncestor->GetContextLinks(&pLinks),
        "IContextNode::GetContextLinks failed");
    ULONG nLinks;
    CheckHResult(pLinks->GetCount(&nLinks), "IContextLinks::GetCount failed");
    for (ULONG i = 0; i < nLinks; i++)
    {
        IContextLink* pLink;
        CheckHResult(pLinks->GetContextLink(i, &pLink),
            "IContextLinks::GetContextLink failed");
        // Check link direction
        ContextLinkDirection linkDirection;
        CheckHResult(pLink->GetContextLinkDirection(&linkDirection),
            "IContextLink:GetContextLinkDirection failed");
        if (linkDirection == ContextLinkDirection_LinksTo)
        {
            // Get source node and add the array
            IContextNode* pSourceNode;
            CheckHResult(pLink->GetSourceNode(&pSourceNode),
                "IContextLink::GetSourceNode failed");
            linkedToNodes.Add(pSourceNode);
        }
    }
            
    // Go up another level
    IContextNode* pNewAncestor;
    CheckHResult(pAncestor->GetParentNode(&pNewAncestor),
        "IContextNode::GetParentNode failed");
    pAncestor = pNewAncestor;
}
```



## <a name="requirements"></a><span data-ttu-id="93b4e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93b4e-118">Requirements</span></span>



| <span data-ttu-id="93b4e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93b4e-119">Requirement</span></span> | <span data-ttu-id="93b4e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="93b4e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93b4e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93b4e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="93b4e-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93b4e-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="93b4e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93b4e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="93b4e-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="93b4e-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="93b4e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="93b4e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="93b4e-126"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="93b4e-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93b4e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93b4e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93b4e-128">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="93b4e-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="93b4e-129">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="93b4e-129">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




