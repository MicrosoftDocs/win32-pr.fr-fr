---
description: Cette section décrit les macros de l’utilitaire Windows Shell.
title: Macros de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5be120f4-bf5d-44b3-b508-20a2104655fa
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 085bca918cfa6ca1441272c3c9181226ef603ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952250"
---
# <a name="shell-macros"></a><span data-ttu-id="e7c0d-103">Macros de Shell</span><span class="sxs-lookup"><span data-stu-id="e7c0d-103">Shell Macros</span></span>

<span data-ttu-id="e7c0d-104">Cette section décrit les macros de l’utilitaire Windows Shell.</span><span class="sxs-lookup"><span data-stu-id="e7c0d-104">This section describes the Windows Shell utility macros.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e7c0d-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="e7c0d-105">In this section</span></span>



| <span data-ttu-id="e7c0d-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="e7c0d-106">Topic</span></span>                                                                  | <span data-ttu-id="e7c0d-107">Description</span><span class="sxs-lookup"><span data-stu-id="e7c0d-107">Description</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7c0d-108">**DÉFINIR \_ PROPERTYKEY**</span><span class="sxs-lookup"><span data-stu-id="e7c0d-108">**DEFINE\_PROPERTYKEY**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-define_propertykey)<br/>           | <span data-ttu-id="e7c0d-109">Utilisé pour empaqueter un identificateur de format (FMTID) et un identificateur de propriété (PID) dans une structure [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) qui représente une clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="e7c0d-109">Used to pack a format identifier (FMTID) and property identifier (PID) into a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure that represents a property key.</span></span><br/>                                                                                    |
| [<span data-ttu-id="e7c0d-110">**IID \_ PPV \_ args**</span><span class="sxs-lookup"><span data-stu-id="e7c0d-110">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)<br/>                      | <span data-ttu-id="e7c0d-111">Utilisé pour récupérer un pointeur d’interface, en fournissant automatiquement la valeur IID de l’interface demandée en fonction du type du pointeur d’interface utilisé.</span><span class="sxs-lookup"><span data-stu-id="e7c0d-111">Used to retrieve an interface pointer, supplying the IID value of the requested interface automatically based on the type of the interface pointer used.</span></span> <span data-ttu-id="e7c0d-112">Cela évite une erreur de codage commune en vérifiant le type de la valeur passée au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="e7c0d-112">This avoids a common coding error by checking the type of the value passed at compile time.</span></span><br/> |
| [<span data-ttu-id="e7c0d-113">**IsEqualPropertyKey**</span><span class="sxs-lookup"><span data-stu-id="e7c0d-113">**IsEqualPropertyKey**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-isequalpropertykey)<br/>            | <span data-ttu-id="e7c0d-114">Compare les membres de deux structures [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) et retourne si elles sont égales.</span><span class="sxs-lookup"><span data-stu-id="e7c0d-114">Compares the members of two [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structures and returns whether they are equal.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="e7c0d-115">**MAKEDLLVERULL**</span><span class="sxs-lookup"><span data-stu-id="e7c0d-115">**MAKEDLLVERULL**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull)<br/>                      | <span data-ttu-id="e7c0d-116">Utilisé pour compresser les informations de version de DLL dans une valeur ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="e7c0d-116">Used to pack DLL version information into a ULONGLONG value.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="e7c0d-117">**DisplayErrorTip NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="e7c0d-117">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)<br/> | <span data-ttu-id="e7c0d-118">Affiche un message d’erreur dans l’info-bulle associée au contrôle d’adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="e7c0d-118">Displays an error message in the balloon tip associated with the network address control.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="e7c0d-119">**GetAddress NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="e7c0d-119">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)<br/>           | <span data-ttu-id="e7c0d-120">Indique si une adresse réseau est conforme à un type et un format spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e7c0d-120">Indicates whether a network address conforms to a specified type and format.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="e7c0d-121">**GetAllowType NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="e7c0d-121">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)<br/>       | <span data-ttu-id="e7c0d-122">Récupère les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.</span><span class="sxs-lookup"><span data-stu-id="e7c0d-122">Retrieves the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="e7c0d-123">**SetAllowType NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="e7c0d-123">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)<br/>       | <span data-ttu-id="e7c0d-124">Définit les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.</span><span class="sxs-lookup"><span data-stu-id="e7c0d-124">Sets the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                     |



 

 

 
