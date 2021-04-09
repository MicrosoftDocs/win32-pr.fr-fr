---
title: Fonctions modales utilisateur
description: Les fonctions modales utilisateur de gestion de réseau obtiennent et définissent des paramètres à l’ensemble du système liés au comportement du système de sécurité.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941298"
---
# <a name="user-modal-functions"></a><span data-ttu-id="3dca0-103">Fonctions modales utilisateur</span><span class="sxs-lookup"><span data-stu-id="3dca0-103">User Modal Functions</span></span>

<span data-ttu-id="3dca0-104">Les fonctions modales utilisateur de gestion de réseau obtiennent et définissent des paramètres à l’ensemble du système liés au comportement du système de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3dca0-104">The network management user modal functions get and set system-wide parameters related to security system behavior.</span></span>

<span data-ttu-id="3dca0-105">Les fonctions modales utilisateur sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3dca0-105">The user modal functions are listed following.</span></span>



| <span data-ttu-id="3dca0-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="3dca0-106">Function</span></span>                                     | <span data-ttu-id="3dca0-107">Description</span><span class="sxs-lookup"><span data-stu-id="3dca0-107">Description</span></span>                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3dca0-108">**NetUserModalsGet**</span><span class="sxs-lookup"><span data-stu-id="3dca0-108">**NetUserModalsGet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | <span data-ttu-id="3dca0-109">Retourne des informations globales pour tous les utilisateurs et groupes globaux dans la base de données de sécurité, qui est la base de données du gestionnaire de comptes de sécurité (SAM) ou, dans le cas des contrôleurs de domaine, la Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3dca0-109">Returns global information for all users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.</span></span> |
| [<span data-ttu-id="3dca0-110">**NetUserModalsSet**</span><span class="sxs-lookup"><span data-stu-id="3dca0-110">**NetUserModalsSet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | <span data-ttu-id="3dca0-111">Définit des informations globales pour tous les utilisateurs et groupes globaux dans la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3dca0-111">Sets global information for all users and global groups in the security database.</span></span>                                                                                                                       |



 

<span data-ttu-id="3dca0-112">Les fonctions **NetUserModalsGet** et **NetUserModalsSet** examinent et modifient les paramètres modaux, qui sont des paramètres globaux qui affectent chaque compte de la base de données de sécurité (par exemple, la longueur minimale autorisée pour le mot de passe).</span><span class="sxs-lookup"><span data-stu-id="3dca0-112">The **NetUserModalsGet** and **NetUserModalsSet** functions examine and modify the modal settings, which are global parameters that affect every account in the security database (for example, the minimum allowable password length).</span></span> <span data-ttu-id="3dca0-113">Tous les paramètres modaux peuvent être modifiés en appelant **NetUserModalsSet**.</span><span class="sxs-lookup"><span data-stu-id="3dca0-113">All modal settings can be altered by calling **NetUserModalsSet**.</span></span> <span data-ttu-id="3dca0-114">La plupart des modaux peuvent également être modifiés à l’aide de la commande **net Accounts** .</span><span class="sxs-lookup"><span data-stu-id="3dca0-114">Most of the modals can also be altered by using the **net accounts** command.</span></span> <span data-ttu-id="3dca0-115">Les fonctions modales de l’utilisateur de gestion de réseau ne nécessitent pas que le serveur dispose d’une sécurité au niveau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3dca0-115">The network management user modal functions do not require the server to have user-level security.</span></span>

<span data-ttu-id="3dca0-116">Les informations modales de l’utilisateur sont disponibles aux niveaux suivants :</span><span class="sxs-lookup"><span data-stu-id="3dca0-116">User modal information is available at the following levels:</span></span>

-   [<span data-ttu-id="3dca0-117">**\_Informations sur les modales utilisateur \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="3dca0-117">**USER\_MODALS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [<span data-ttu-id="3dca0-118">**\_Informations sur les modaux utilisateur \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="3dca0-118">**USER\_MODALS\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [<span data-ttu-id="3dca0-119">**\_Informations sur les modales utilisateur \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="3dca0-119">**USER\_MODALS\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [<span data-ttu-id="3dca0-120">**Informations sur les modaux de l’utilisateur \_ \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="3dca0-120">**USER\_MODALS\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

<span data-ttu-id="3dca0-121">Les niveaux d’informations suivants sont valides uniquement pour [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) et remplacent l’ancien moyen de passer un *Parmnum* pour définir un champ spécifique :</span><span class="sxs-lookup"><span data-stu-id="3dca0-121">The following information levels are valid only for [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) and replace the older way of passing in a *Parmnum* to set a specific field:</span></span>

-   [<span data-ttu-id="3dca0-122">**\_Informations sur les modaux utilisateur \_ \_ 1001**</span><span class="sxs-lookup"><span data-stu-id="3dca0-122">**USER\_MODALS\_INFO\_1001**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [<span data-ttu-id="3dca0-123">**\_Informations sur les modaux utilisateur \_ \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="3dca0-123">**USER\_MODALS\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [<span data-ttu-id="3dca0-124">**\_Informations sur les modaux utilisateur \_ \_ 1003**</span><span class="sxs-lookup"><span data-stu-id="3dca0-124">**USER\_MODALS\_INFO\_1003**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [<span data-ttu-id="3dca0-125">**\_Informations sur les modaux utilisateur \_ \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="3dca0-125">**USER\_MODALS\_INFO\_1004**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [<span data-ttu-id="3dca0-126">**\_Informations sur les modaux utilisateur \_ \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="3dca0-126">**USER\_MODALS\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [<span data-ttu-id="3dca0-127">**\_Informations sur les modaux utilisateur \_ \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="3dca0-127">**USER\_MODALS\_INFO\_1006**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [<span data-ttu-id="3dca0-128">**\_Informations sur les modaux utilisateur \_ \_ 1007**</span><span class="sxs-lookup"><span data-stu-id="3dca0-128">**USER\_MODALS\_INFO\_1007**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

<span data-ttu-id="3dca0-129">Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions modales utilisateur de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="3dca0-129">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user modal functions.</span></span> <span data-ttu-id="3dca0-130">Pour plus d’informations, consultez [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span><span class="sxs-lookup"><span data-stu-id="3dca0-130">For more information, see [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span></span>

 

 