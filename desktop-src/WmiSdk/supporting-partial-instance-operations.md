---
description: Un fournisseur n’est pas requis pour prendre en charge les opérations d’instance partielle. Toutefois, un fournisseur doit prendre en charge toutes les sémantiques d’une opération d’instance partielle, traiter une instance complète ou retourner un \_ \_ paramètre non pris en charge par WBEM \_ .
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Prise en charge des opérations de Partial-Instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf656688ffbcc6981c6a3e55dc480570ad0f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524128"
---
# <a name="supporting-partial-instance-operations"></a><span data-ttu-id="b4907-104">Prise en charge des opérations de Partial-Instance</span><span class="sxs-lookup"><span data-stu-id="b4907-104">Supporting Partial-Instance Operations</span></span>

<span data-ttu-id="b4907-105">Un fournisseur n’est pas requis pour prendre en charge les opérations d’instance partielle.</span><span class="sxs-lookup"><span data-stu-id="b4907-105">A provider is not required to support any partial-instance operations.</span></span> <span data-ttu-id="b4907-106">Toutefois, un fournisseur doit prendre en charge toutes les sémantiques d’une opération d’instance partielle, traiter une instance complète ou retourner **un \_ \_ \_ paramètre non pris en charge par WBEM**.</span><span class="sxs-lookup"><span data-stu-id="b4907-106">However, a provider must either support all the semantics of a partial-instance operation, process a complete instance, or return **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="b4907-107">Lorsque vous créez un fournisseur qui prend en charge les opérations d’instance partielle, vous devez respecter les règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4907-107">When creating a provider that supports partial-instance operations, you must observe the following rules:</span></span>

-   <span data-ttu-id="b4907-108">Réutilisez le même objet de contexte que WMI pour envoyer au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b4907-108">Reuse the same context object that WMI sends to the provider.</span></span> <span data-ttu-id="b4907-109">WMI utilise la \_ \_ \_ valeur nommée « obtenir ext \_ client \_ Request » pour éviter les interblocages et supprime ce client avant de transférer l’objet de contexte à un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b4907-109">WMI uses the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value to prevent deadlocks and removes this client before forwarding the context object to a provider.</span></span>
-   <span data-ttu-id="b4907-110">Pour les rappels réentrants dans WMI qui ne nécessitent pas d’opération d’instance partielle, assurez-vous de renvoyer le même objet de contexte sans aucune modification.</span><span class="sxs-lookup"><span data-stu-id="b4907-110">For reentrant calls back into WMI that do not require a partial-instance operation, ensure to pass back the same context object without any modifications.</span></span> <span data-ttu-id="b4907-111">WMI reçoit l’objet de contexte sans la \_ \_ \_ valeur nommée « obtenir ext \_ client \_ Request » définie et supprime toutes les valeurs nommées associées à des opérations d’instance partielle de l’objet de contexte avant de le passer à d’autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="b4907-111">WMI receives the context object without the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value set and deletes all named values associated with partial-instance operations from the context object before passing it to other providers.</span></span> <span data-ttu-id="b4907-112">Le fait de ne pas modifier l’objet de contexte empêche les autres fournisseurs de recevoir des opérations de récupération d’instance partielle destinées à un objet différent et non lié.</span><span class="sxs-lookup"><span data-stu-id="b4907-112">Not changing the context object blocks other providers from receiving partial-instance retrieval operations intended for a different, unrelated object.</span></span>
-   <span data-ttu-id="b4907-113">Pour effectuer une opération d’instance partielle réentrante pendant l’exécution d’une requête, définissez la \_ \_ \_ valeur nommée « obtenir ext \_ client Request » manquante et la \_ propriété Clear.</span><span class="sxs-lookup"><span data-stu-id="b4907-113">To perform a reentrant partial-instance operation while carrying out a request, set the missing "\_\_GET\_EXT\_CLIENT\_REQUEST" named value and property clear.</span></span> <span data-ttu-id="b4907-114">Si vous le souhaitez, vous pouvez modifier les propriétés de la \_ \_ \_ valeur nommée « récupérer \_ les propriétés ext » avant de renvoyer l’objet de contexte dans WMI avec l’appel réentrant.</span><span class="sxs-lookup"><span data-stu-id="b4907-114">Optionally, you can modify the properties in the "\_\_GET\_EXT\_PROPERTIES" named value before sending the context object back into WMI with the reentrant call.</span></span>
-   <span data-ttu-id="b4907-115">N’accédez pas à l’objet de contexte après l’avoir retourné à WMI lors d’un appel réentrant ; d’autres fournisseurs peuvent modifier les listes de propriétés ou d’autres valeurs pendant la réentrance.</span><span class="sxs-lookup"><span data-stu-id="b4907-115">Do not access the context object after you return it to WMI during a reentrant call; other providers may modify the property lists or other values during reentrancy.</span></span> <span data-ttu-id="b4907-116">Vous pouvez examiner ou modifier l’objet de contexte uniquement pendant la durée de l’appel [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que vous implémentez.</span><span class="sxs-lookup"><span data-stu-id="b4907-116">You can examine or modify the context object only for the duration of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call that you implement.</span></span>

 

 



