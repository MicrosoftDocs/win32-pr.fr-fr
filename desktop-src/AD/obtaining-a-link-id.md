---
title: Obtention d’un ID de lien
description: À compter de Windows Server 2003, il n’est plus nécessaire de demander un linkID de Microsoft ; Il existe un processus pour générer automatiquement un linkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Obtention d’un ID de lien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101440"
---
# <a name="obtaining-a-link-id"></a><span data-ttu-id="4435d-104">Obtention d’un ID de lien</span><span class="sxs-lookup"><span data-stu-id="4435d-104">Obtaining a Link ID</span></span>

<span data-ttu-id="4435d-105">À compter de Windows Server 2003, il n’est plus nécessaire de demander un [**LinkId**](/windows/desktop/ADSchema/a-linkid) de Microsoft ; Il existe un processus pour générer automatiquement un **LinkId**.</span><span class="sxs-lookup"><span data-stu-id="4435d-105">Starting with Windows Server 2003, it is no longer necessary to request a [**linkID**](/windows/desktop/ADSchema/a-linkid) from Microsoft; there is a process for automatically generating a **linkID**.</span></span> <span data-ttu-id="4435d-106">Le système génère automatiquement un ID de lien pour un nouvel attribut lié lorsque l’attribut **LinkId** de l’attribut a la valeur 1.2.840.113556.1.2.50.</span><span class="sxs-lookup"><span data-stu-id="4435d-106">The system will automatically generate a link ID for a new linked attribute when the attribute's **linkID** attribute is set to 1.2.840.113556.1.2.50.</span></span> <span data-ttu-id="4435d-107">Pour créer un lien précédent pour ce lien suivant, affectez au paramètre **LinkId** la valeur [**AttributeID**](/windows/desktop/ADSchema/a-attributeid) ou [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) du lien suivant.</span><span class="sxs-lookup"><span data-stu-id="4435d-107">A back link for this forward link is created by setting the **linkID** to the [**attributeID**](/windows/desktop/ADSchema/a-attributeid) or [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) of the forward link.</span></span> <span data-ttu-id="4435d-108">Le cache de schéma doit être rechargé après la création du lien suivant et avant la création du lien précédent.</span><span class="sxs-lookup"><span data-stu-id="4435d-108">The schema cache must be reloaded after creating the forward link and before creating the back link.</span></span> <span data-ttu-id="4435d-109">Dans le cas contraire, l' **AttributeID** ou le **ldapDisplayName** du lien Forward ne sera pas trouvé lors de la création du lien précédent.</span><span class="sxs-lookup"><span data-stu-id="4435d-109">Otherwise, the forward link's **attributeId** or **ldapDisplayName** will not be found when the back link is created.</span></span> <span data-ttu-id="4435d-110">Le cache de schéma est rechargé à la demande, quelques minutes après qu’une modification de schéma a été effectuée ou lorsque le contrôleur de périphérique est redémarré.</span><span class="sxs-lookup"><span data-stu-id="4435d-110">The schema cache is reloaded on demand, a few minutes after a schema change is made, or when the DC is restarted.</span></span> <span data-ttu-id="4435d-111">Créez tous les liens de transfert, rechargez le cache de schéma, puis créez tous les liens de retour.</span><span class="sxs-lookup"><span data-stu-id="4435d-111">Create all forward links, reload the schema cache and then create all back links.</span></span>

<span data-ttu-id="4435d-112">Par exemple, lorsque vous avez créé les nouveaux attributs **myForwardLinkAttr** et **myBackLinkAttr**, et que vous souhaitez les lier :</span><span class="sxs-lookup"><span data-stu-id="4435d-112">For example, when you have created the new attributes **myForwardLinkAttr** and **myBackLinkAttr**, and wish to link them:</span></span>

> [!Note]  
> <span data-ttu-id="4435d-113">Dans cet exemple, les OID sont fictif.</span><span class="sxs-lookup"><span data-stu-id="4435d-113">The OIDs in this example are contrived.</span></span> <span data-ttu-id="4435d-114">Consultez [obtention d’un identificateur d’objet auprès de Microsoft](obtaining-an-object-identifier-from-microsoft.md) pour obtenir des instructions sur l’obtention d’OID pour les nouveaux attributs.</span><span class="sxs-lookup"><span data-stu-id="4435d-114">See [Obtaining an Object Identifier from Microsoft](obtaining-an-object-identifier-from-microsoft.md) for instructions on obtaining OIDs for new attributes.</span></span>

 

1.  <span data-ttu-id="4435d-115">Définissez ces attributs sur l’attribut qui doit être le lien suivant :</span><span class="sxs-lookup"><span data-stu-id="4435d-115">Set these attributes on the attribute that is to be the forward link:</span></span>
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  <span data-ttu-id="4435d-116">Rechargez le schéma.</span><span class="sxs-lookup"><span data-stu-id="4435d-116">Reload the Schema.</span></span>
3.  <span data-ttu-id="4435d-117">Définissez ces attributs sur l’attribut qui doit être le lien précédent :</span><span class="sxs-lookup"><span data-stu-id="4435d-117">Set these attributes on the attribute that is to be the back link:</span></span>
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a><span data-ttu-id="4435d-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4435d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4435d-119">Attributs liés</span><span class="sxs-lookup"><span data-stu-id="4435d-119">Linked Attributes</span></span>](linked-attributes.md)
</dt> <dt>

[<span data-ttu-id="4435d-120">Comment étendre le schéma</span><span class="sxs-lookup"><span data-stu-id="4435d-120">How to Extend the Schema</span></span>](how-to-extend-the-schema.md)
</dt> </dl>

 

 