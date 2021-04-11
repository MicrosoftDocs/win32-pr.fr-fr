---
title: InvalidSecurityDescriptorLoggingLevel
description: Définit le niveau de détail des entrées du journal des événements sur les descripteurs de sécurité non valides pour le lancement et les autorisations d’accès des composants.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Valeur de Registre InvalidSecurityDescriptorLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309181"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a><span data-ttu-id="df5e6-104">InvalidSecurityDescriptorLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="df5e6-104">InvalidSecurityDescriptorLoggingLevel</span></span>

<span data-ttu-id="df5e6-105">Définit le niveau de détail des entrées du journal des événements sur les descripteurs de sécurité non valides pour le lancement et les autorisations d’accès des composants.</span><span class="sxs-lookup"><span data-stu-id="df5e6-105">Sets the verbosity of event log entries about invalid security descriptors for component launch and access permissions.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="df5e6-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="df5e6-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="df5e6-107">Notes</span><span class="sxs-lookup"><span data-stu-id="df5e6-107">Remarks</span></span>

<span data-ttu-id="df5e6-108">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="df5e6-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="df5e6-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="df5e6-109">Value</span></span> | <span data-ttu-id="df5e6-110">Description</span><span class="sxs-lookup"><span data-stu-id="df5e6-110">Description</span></span>                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df5e6-111">1</span><span class="sxs-lookup"><span data-stu-id="df5e6-111">1</span></span>     | <span data-ttu-id="df5e6-112">Consigne toujours les échecs quand COM détecte un descripteur de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="df5e6-112">Always log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="df5e6-113">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="df5e6-113">This is the default value.</span></span>                                                                                  |
| <span data-ttu-id="df5e6-114">2</span><span class="sxs-lookup"><span data-stu-id="df5e6-114">2</span></span>     | <span data-ttu-id="df5e6-115">Ne consigne jamais les échecs quand COM détecte un descripteur de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="df5e6-115">Never log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="df5e6-116">Il n’est pas recommandé de désactiver la journalisation des événements, car cela peut compliquer le diagnostic des problèmes.</span><span class="sxs-lookup"><span data-stu-id="df5e6-116">It is not recommended that you disable event logging, as it can make it more difficult to diagnose problems.</span></span> |



 

<span data-ttu-id="df5e6-117">Si vous définissez directement les descripteurs de sécurité des autorisations d’exécution et d’accès (généralement appelées ACL), il est possible de construire un descripteur de sécurité dont la signification ne peut pas être interprétée sans ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="df5e6-117">If you set launch and access permission security descriptors (commonly called ACLs) directly, it is possible to construct a security descriptor whose meaning cannot be interpreted unambiguously.</span></span> <span data-ttu-id="df5e6-118">COM crée une entrée dans le journal des événements lorsqu’il rencontre un descripteur de sécurité non valide.</span><span class="sxs-lookup"><span data-stu-id="df5e6-118">COM makes an event log entry when it encounters such an invalid security descriptor.</span></span>

<span data-ttu-id="df5e6-119">Notez que [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) et [**CallFailureLoggingLevel**](callfailurelogginglevel.md) n’ont aucun contrôle sur la journalisation des erreurs de descripteur de sécurité non valides.</span><span class="sxs-lookup"><span data-stu-id="df5e6-119">Note that [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) and [**CallFailureLoggingLevel**](callfailurelogginglevel.md) have no control over logging invalid security descriptor errors.</span></span> <span data-ttu-id="df5e6-120">Utilisez **InvalidSecurityDescriptorLoggingLevel** pour un contrôle total de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="df5e6-120">Use **InvalidSecurityDescriptorLoggingLevel** for full control over this functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df5e6-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df5e6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df5e6-122">Définition de la sécurité pour les applications COM</span><span class="sxs-lookup"><span data-stu-id="df5e6-122">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




