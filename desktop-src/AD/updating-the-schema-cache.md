---
title: Mise à jour du cache de schéma
description: Toutes les informations écrites sur un serveur Active Directory sont validées par rapport au schéma.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Mise à jour de la publicité du cache de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671210"
---
# <a name="updating-the-schema-cache"></a><span data-ttu-id="cad72-104">Mise à jour du cache de schéma</span><span class="sxs-lookup"><span data-stu-id="cad72-104">Updating the Schema Cache</span></span>

<span data-ttu-id="cad72-105">Toutes les informations écrites sur un serveur Active Directory sont validées par rapport au schéma.</span><span class="sxs-lookup"><span data-stu-id="cad72-105">All information that is written to an Active Directory server is validated against the schema.</span></span> <span data-ttu-id="cad72-106">Le schéma est conservé en mémoire sur les serveurs d’annuaire (contrôleurs de domaine) pour des raisons de performances.</span><span class="sxs-lookup"><span data-stu-id="cad72-106">The schema is held in memory on directory servers (domain controllers) for performance reasons.</span></span> <span data-ttu-id="cad72-107">La version en mémoire est mise à jour automatiquement après la mise à jour de la version sur disque.</span><span class="sxs-lookup"><span data-stu-id="cad72-107">The in-memory version is updated automatically after the on-disk version has been updated.</span></span> <span data-ttu-id="cad72-108">La mise à jour automatique se produit cinq minutes après l’application de la dernière modification. l’application d’une autre modification au schéma dans la fenêtre de 5 minutes réinitialise la minuterie pendant 5 minutes.</span><span class="sxs-lookup"><span data-stu-id="cad72-108">The automatic update occurs five minutes after the last change was applied; applying another change to the schema in the 5-minute window resets the timer for another 5 minutes.</span></span> <span data-ttu-id="cad72-109">Ce comportement garantit la cohérence du cache, mais peut prêter à confusion, car les modifications n’apparaissent pas dans le schéma tant que le cache n’est pas mis à jour, même s’ils ont été appliqués sur le disque.</span><span class="sxs-lookup"><span data-stu-id="cad72-109">This behavior keeps the cache consistent, but can be confusing, because changes do not appear in the schema until the cache is updated, even though they were applied on disk.</span></span>

<span data-ttu-id="cad72-110">Pour mettre à jour le cache de schéma Active Directory après une mise à jour du schéma, ou si vous souhaitez utiliser immédiatement la mise à jour du schéma pour les opérations sans schéma, ajoutez l’attribut **schemaUpdateNow** (il s’agit d’un attribut opérationnel) au DSE racine (nom de domaine vide) avec la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="cad72-110">To update the Active Directory schema cache after a schema update, or if you want to use the schema update for non-schema operations immediately, add the **schemaUpdateNow** attribute (it is an operational attribute) to the root DSE (blank DN) with value 1.</span></span> <span data-ttu-id="cad72-111">Une mise à jour du cache de schéma démarrera immédiatement.</span><span class="sxs-lookup"><span data-stu-id="cad72-111">A schema cache update will start immediately.</span></span> <span data-ttu-id="cad72-112">L’appel est bloquant.</span><span class="sxs-lookup"><span data-stu-id="cad72-112">The call is blocking.</span></span> <span data-ttu-id="cad72-113">Si l’appel retourne sans erreur, le cache est mis à jour et toutes les mises à jour de schéma sont prêtes à être utilisées.</span><span class="sxs-lookup"><span data-stu-id="cad72-113">If the call returns with no error, the cache is updated and all schema updates are ready to be used.</span></span> <span data-ttu-id="cad72-114">Un retour d’erreur indique que la mise à jour du cache a échoué.</span><span class="sxs-lookup"><span data-stu-id="cad72-114">An error return indicates the cache update was unsuccessful.</span></span> <span data-ttu-id="cad72-115">Les applications qui doivent utiliser cette fonctionnalité doivent être conçues pour prendre en charge l’écriture de blocage, en particulier pour donner des commentaires à l’utilisateur, si le programme ou le script s’exécute de manière interactive.</span><span class="sxs-lookup"><span data-stu-id="cad72-115">Applications that must use this feature should be designed to accommodate the blocking write, particularly in giving the user feedback, if the program or script executes interactively.</span></span>

<span data-ttu-id="cad72-116">L’exemple de code suivant est un exemple de script LDIFDE qui montre comment déclencher un rechargement du cache.</span><span class="sxs-lookup"><span data-stu-id="cad72-116">The following code example is a sample LDIFDE script that shows how to trigger a cache reload.</span></span>

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

<span data-ttu-id="cad72-117">Pour plus d’informations sur la mise à jour du cache de schéma par programme, consultez [l’exemple de code pour la mise à jour du cache de schéma](example-code-for-updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="cad72-117">For more information about how to update the schema cache programmatically, see [Example Code for Updating the Schema Cache](example-code-for-updating-the-schema-cache.md).</span></span>

 

 




