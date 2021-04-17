---
title: Conditions préalables à l’installation d’une extension de schéma
description: Pour modifier le schéma, assurez-vous de disposer des droits suivants et tenez compte des informations suivantes. vous devez disposer des droits suffisants pour modifier le schéma.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 275f468df54b9ced3dcca0648e4cc3602ab71422
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314372"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a><span data-ttu-id="72844-103">Conditions préalables à l’installation d’une extension de schéma</span><span class="sxs-lookup"><span data-stu-id="72844-103">Prerequisites for Installing a Schema Extension</span></span>

<span data-ttu-id="72844-104">Pour modifier le schéma, assurez-vous de disposer des droits suivants et tenez compte des informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="72844-104">To modify the schema, ensure you have the following rights and are aware of the following information:</span></span>

-   <span data-ttu-id="72844-105">Vous devez disposer des droits suffisants pour modifier le schéma.</span><span class="sxs-lookup"><span data-stu-id="72844-105">You must have sufficient rights to modify the schema.</span></span> <span data-ttu-id="72844-106">Le schéma contient toutes les définitions de données pour Active Directory Domain Services pour l’ensemble de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="72844-106">The schema contains all of the data definitions for Active Directory Domain Services for the entire enterprise.</span></span> <span data-ttu-id="72844-107">Pour mettre à jour le schéma, un utilisateur doit être membre du groupe administrateurs du schéma, ou les droits de mise à jour du schéma ont été délégués.</span><span class="sxs-lookup"><span data-stu-id="72844-107">To update the schema, a user must be a member of the Schema Administrators group, or have been delegated the rights to update the schema.</span></span>
-   <span data-ttu-id="72844-108">Vous ne pouvez apporter des modifications de schéma qu’au contrôleur de schéma.</span><span class="sxs-lookup"><span data-stu-id="72844-108">You can only make schema changes at the schema master.</span></span> <span data-ttu-id="72844-109">Pour plus d’informations, consultez [détection du contrôleur de schéma](detecting-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="72844-109">For more information, see [Detecting the Schema Master](detecting-the-schema-master.md).</span></span>
-   <span data-ttu-id="72844-110">Le contrôleur de schéma doit être accessible en écriture ; autrement dit, le verrouillage de sécurité dans le registre doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="72844-110">The schema master must be writable; that is, the safety interlock in the registry must be removed.</span></span> <span data-ttu-id="72844-111">Pour plus d’informations, consultez [la page activation des modifications de schéma sur le contrôleur de schéma](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="72844-111">For more information, see [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
-   <span data-ttu-id="72844-112">Pour plus d’informations sur la façon de vérifier si le contrôleur de schéma peut être modifié et sur la façon de modifier ses paramètres, consultez « XADM : impossible de mettre à jour le schéma sur le propriétaire du schéma » dans la base de connaissances d’aide et de support à l’adresse [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span><span class="sxs-lookup"><span data-stu-id="72844-112">For more information about how to check whether the schema master can be modified, and how to change its settings, see "XADM: Unable to Update the Schema on the Schema Owner" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span></span>

 

 




