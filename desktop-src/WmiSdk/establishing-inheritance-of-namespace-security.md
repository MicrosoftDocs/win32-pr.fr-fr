---
description: Vous pouvez contrôler si un espace de noms enfant hérite du descripteur de sécurité de l’espace de noms parent.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Établissement de l’héritage de la sécurité des espaces de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e242299b78ede3ff49679305a97823bc022358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528325"
---
# <a name="establishing-inheritance-of-namespace-security"></a><span data-ttu-id="d4d63-103">Établissement de l’héritage de la sécurité des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="d4d63-103">Establishing Inheritance of Namespace Security</span></span>

<span data-ttu-id="d4d63-104">Vous pouvez contrôler si un espace de noms enfant hérite du descripteur de sécurité de l’espace de noms parent.</span><span class="sxs-lookup"><span data-stu-id="d4d63-104">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

<span data-ttu-id="d4d63-105">Les espaces de noms WMI ont des descripteurs de sécurité qui contrôlent qui peut accéder à l’espace de noms et aux données de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d4d63-105">WMI namespaces have security descriptors that control who can access the namespace and the data of the namespace.</span></span> <span data-ttu-id="d4d63-106">Chaque descripteur de sécurité a une liste de contrôle d’accès discrétionnaire (DACL) et une liste de contrôle d’accès de sécurité (SACL).</span><span class="sxs-lookup"><span data-stu-id="d4d63-106">Each security descriptor has a discretionary access control list (DACL) and a security access control list (SACL).</span></span> <span data-ttu-id="d4d63-107">Ces listes contiennent des entrées de contrôle d’accès (ACE).</span><span class="sxs-lookup"><span data-stu-id="d4d63-107">These lists contain access control entries (ACE).</span></span>

<span data-ttu-id="d4d63-108">En fonction des [**constantes d’indicateur d’entrée**](namespace-ace-flag-constants.md) du contrôle d’accès de l’espace de noms définies, les autorisations appliquées à un espace de noms peuvent être héritées par tous les espaces de noms enfants de cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d4d63-108">Depending on the [**Namespace ACE Flag Constants**](namespace-ace-flag-constants.md) that are set, permissions that are applied to a namespace may be inherited by all the child namespaces of that namespace.</span></span> <span data-ttu-id="d4d63-109">Un espace de noms enfant hérite du descripteur de sécurité de son espace de noms parent lorsque l’espace de noms enfant est créé si l’indicateur **\_ \_ ACE inherit du conteneur** se trouve dans le descripteur de sécurité de l’espace de noms parent.</span><span class="sxs-lookup"><span data-stu-id="d4d63-109">A child namespace inherits the security descriptor of its parent namespace when the child namespace is created if the **CONTAINER\_INHERIT\_ACE** flag is in the parent namespace security descriptor.</span></span> <span data-ttu-id="d4d63-110">Si le **conteneur hérite de l’entrée de contrôle d’accès, l’entrée de contrôle d’accès n’hérite pas \_ \_ \| \_ se propager \_ \_** est définie.</span><span class="sxs-lookup"><span data-stu-id="d4d63-110">If **CONTAINER\_INHERIT\_ACE\|NO\_PROPOGATE\_INHERIT\_ACE** is set, then only the child namespace inherits the security descriptor, not grandchild namespaces.</span></span> <span data-ttu-id="d4d63-111">Les espaces de noms enfants peuvent remplacer les autorisations de sécurité de leur parent en appelant des méthodes de la classe [**\_ \_ SystemSecurity**](--systemsecurity.md) pour écrire un nouveau descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d4d63-111">Child namespaces can override the security permissions of their parent by calling methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class to write a new security descriptor.</span></span> <span data-ttu-id="d4d63-112">Les paramètres de sécurité par défaut ne peuvent pas être modifiés.</span><span class="sxs-lookup"><span data-stu-id="d4d63-112">The default security settings cannot be changed.</span></span> <span data-ttu-id="d4d63-113">Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md). Pour plus d’informations sur les DACL, consultez [listes de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) et [**constantes de type ACE d’espace de noms**](namespace-ace-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d4d63-113">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).For more information about DACLs, see [Access Control Lists (ACL)](/windows/desktop/SecAuthZ/access-control-lists) and [**Namespace ACE Type Constants**](namespace-ace-type-constants.md).</span></span>

<span data-ttu-id="d4d63-114">Notez que les autorisations par défaut ne peuvent pas être modifiées.</span><span class="sxs-lookup"><span data-stu-id="d4d63-114">Note that the default permissions cannot be changed.</span></span> <span data-ttu-id="d4d63-115">En outre, la définition de l’indicateur de **\_ \_ protection discrétionnaire** de l’ingénieur de sécurité en définissant le descripteur de sécurité (SD) n’est pas utilisée pour ajouter un SD spécialisé à un espace de noms enfant.</span><span class="sxs-lookup"><span data-stu-id="d4d63-115">Furthermore, setting the **SE\_DACL\_PROTECTED** flag while setting the security descriptor (SD) is not used to add a specialized SD to a child namespace.</span></span> <span data-ttu-id="d4d63-116">Pour remplacer un SD hérité, il vous suffit d’en définir un nouveau.</span><span class="sxs-lookup"><span data-stu-id="d4d63-116">To override an inherited SD, simply set a new one.</span></span> <span data-ttu-id="d4d63-117">Pour hériter de ce SD sur un espace de noms enfant, transmettez l’indicateur **\_ \_ ACE inherit au conteneur** dans le descripteur de sécurité de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d4d63-117">To inherit that SD to a child namespace, pass the **CONTAINER\_INHERIT\_ACE** flag in the namespace security descriptor.</span></span> <span data-ttu-id="d4d63-118">Pour hériter uniquement de l’enfant, et non des descendants, passer `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span><span class="sxs-lookup"><span data-stu-id="d4d63-118">To inherit to just the child, and not the descendants, pass `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span></span>

<span data-ttu-id="d4d63-119">.</span><span class="sxs-lookup"><span data-stu-id="d4d63-119">.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4d63-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d4d63-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4d63-121">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="d4d63-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="d4d63-122">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="d4d63-122">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 
