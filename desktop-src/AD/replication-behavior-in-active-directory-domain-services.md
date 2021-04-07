---
title: Comportement de réplication dans Active Directory Domain Services
description: Le comportement de réplication est cohérent et prévisible ; étant donné un ensemble de modifications apportées à un réplica donné, le résultat peut être prédit \ 8212 ; les modifications sont propagées à tous les autres réplicas.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, réplication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41009a733f99366e499a25baca989f4f28794aea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839270"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a><span data-ttu-id="ff4ee-104">Comportement de réplication dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="ff4ee-104">Replication Behavior in Active Directory Domain Services</span></span>

<span data-ttu-id="ff4ee-105">Le comportement de réplication est cohérent et prévisible ; étant donné un ensemble de modifications apportées à un réplica donné, le résultat peut être prédit. les modifications seront propagées à tous les autres réplicas.</span><span class="sxs-lookup"><span data-stu-id="ff4ee-105">Replication behavior is consistent and predictable; given a set of changes to a given replica, the outcome can be predicted—the changes will be propagated to all other replicas.</span></span> <span data-ttu-id="ff4ee-106">La conception d’un modèle général fiable pour prédire quand les modifications seront appliquées à tous les autres réplicas, ou à un réplica particulier, est impossible, car l’état futur du système distribué dans son ensemble ne peut pas être connu.</span><span class="sxs-lookup"><span data-stu-id="ff4ee-106">Devising a reliable general model for predicting when the changes will be applied at all other replicas, or at a particular replica, is impossible, because the future state of the distributed system as a whole cannot be known.</span></span> <span data-ttu-id="ff4ee-107">C’est ce que l’on appelle la « latence non déterministe » et les applications qui utilisent le répertoire doivent comprendre et autoriser ce dernier.</span><span class="sxs-lookup"><span data-stu-id="ff4ee-107">This is called "nondeterministic latency," and applications that use the directory must understand and allow for it.</span></span>

<span data-ttu-id="ff4ee-108">La situation n’est pas aussi complexe au moment où elle peut apparaître.</span><span class="sxs-lookup"><span data-stu-id="ff4ee-108">The situation is not as complex at it might appear.</span></span> <span data-ttu-id="ff4ee-109">Une application doit prendre en charge uniquement les trois États suivants :</span><span class="sxs-lookup"><span data-stu-id="ff4ee-109">There are only three states that an application must accommodate:</span></span>

-   <span data-ttu-id="ff4ee-110">Décalage de version : aucune des modifications appliquées à un réplica source donné n’a été propagée à un réplica de destination donné.</span><span class="sxs-lookup"><span data-stu-id="ff4ee-110">Version Skew: None of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="ff4ee-111">Une application qui lit le réplica source voit la nouvelle version des informations, tandis qu’une application lisant la destination voit l’ancienne version (ou rien, si les nouvelles informations ont été ajoutées pour la première fois).</span><span class="sxs-lookup"><span data-stu-id="ff4ee-111">An application reading the source replica sees the new version of the information, while an application reading the destination sees the old version (or nothing, if the new information was added for the first time).</span></span> <span data-ttu-id="ff4ee-112">La distorsion de version s’applique à tous les consommateurs de service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="ff4ee-112">Version skew applies to all directory service consumers.</span></span>
-   <span data-ttu-id="ff4ee-113">Mise à jour partielle : certaines des modifications appliquées à un réplica source donné ont été propagées à un réplica de destination donné.</span><span class="sxs-lookup"><span data-stu-id="ff4ee-113">Partial Update: Some of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="ff4ee-114">Une application qui lit le réplica source voit les nouvelles informations, tandis qu’une application qui lit la destination voit une combinaison d’anciennes et de nouvelles informations (ou seulement certaines des nouvelles informations si les nouvelles informations ont été ajoutées pour la première fois).</span><span class="sxs-lookup"><span data-stu-id="ff4ee-114">An application reading the source replica sees the new information, while an application reading the destination sees a mix of old and new information (or only some of the new information, if the new information was added for the first time).</span></span> <span data-ttu-id="ff4ee-115">La mise à jour partielle s’applique aux consommateurs de service d’annuaire qui utilisent deux objets connexes ou plus pour stocker leurs informations.</span><span class="sxs-lookup"><span data-stu-id="ff4ee-115">Partial update applies to directory service consumers that use two or more related objects to store their information.</span></span>
-   <span data-ttu-id="ff4ee-116">État de la réplication complète : toutes les modifications appliquées à un réplica source donné ont été propagées à un réplica de destination donné.</span><span class="sxs-lookup"><span data-stu-id="ff4ee-116">Fully Replicated State: All of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="ff4ee-117">Les applications sur les réplicas de source et de destination voient les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="ff4ee-117">Applications at the source and destination replicas see the same information.</span></span>

 

 




