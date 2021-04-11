---
title: Gestion de la stratégie de retransmission
description: L’application WinSNMP peut demander que l’implémentation de l’WinSNMP Microsoft exécute la stratégie de retransmission de l’application. Lorsque l’implémentation gère la retransmission, elle utilise le délai d’attente et les valeurs du nombre de tentatives dans sa base de données.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029540"
---
# <a name="managing-the-retransmission-policy"></a><span data-ttu-id="776d5-104">Gestion de la stratégie de retransmission</span><span class="sxs-lookup"><span data-stu-id="776d5-104">Managing the Retransmission Policy</span></span>

<span data-ttu-id="776d5-105">L’application WinSNMP peut demander que l’implémentation de l’WinSNMP Microsoft exécute la stratégie de retransmission de l’application.</span><span class="sxs-lookup"><span data-stu-id="776d5-105">The WinSNMP application can request that the Microsoft WinSNMP implementation execute the application's retransmission policy.</span></span> <span data-ttu-id="776d5-106">Lorsque l’implémentation gère la retransmission, elle utilise le délai d’attente et les valeurs du nombre de tentatives dans sa base de données.</span><span class="sxs-lookup"><span data-stu-id="776d5-106">When the implementation manages retransmission, it uses the time-out period and the retry count values in its database.</span></span>

<span data-ttu-id="776d5-107">L’implémentation identifie le mode de retransmission par défaut dans une valeur de retour de la fonction [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="776d5-107">The implementation identifies the default retransmission mode in a return value from the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function during initialization.</span></span> <span data-ttu-id="776d5-108">Le mode peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="776d5-108">The mode can be one of the following values.</span></span>



| <span data-ttu-id="776d5-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="776d5-109">Value</span></span>        | <span data-ttu-id="776d5-110">Signification</span><span class="sxs-lookup"><span data-stu-id="776d5-110">Meaning</span></span>                                                                      |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="776d5-111">SNMPAPI \_ sur</span><span class="sxs-lookup"><span data-stu-id="776d5-111">SNMPAPI\_ON</span></span>  | <span data-ttu-id="776d5-112">L’implémentation exécute la stratégie de retransmission de l’application.</span><span class="sxs-lookup"><span data-stu-id="776d5-112">The implementation is executing the application's retransmission policy.</span></span>     |
| <span data-ttu-id="776d5-113">SNMPAPI \_ désactivé</span><span class="sxs-lookup"><span data-stu-id="776d5-113">SNMPAPI\_OFF</span></span> | <span data-ttu-id="776d5-114">L’implémentation n’exécute pas la stratégie de retransmission de l’application.</span><span class="sxs-lookup"><span data-stu-id="776d5-114">The implementation is not executing the application's retransmission policy.</span></span> |



 

<span data-ttu-id="776d5-115">Une application WinSNMP peut récupérer à tout moment le mode de retransmission en vigueur pour l’implémentation en appelant la fonction [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="776d5-115">A WinSNMP application can retrieve at any time the current retransmission mode in effect for the implementation by calling the [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) function.</span></span> <span data-ttu-id="776d5-116">L’API WinSNMP fournit d’autres [fonctions de base de données](winsnmp-functions.md) qui simplifient la gestion de la stratégie de retransmission.</span><span class="sxs-lookup"><span data-stu-id="776d5-116">The WinSNMP API provides other [database functions](winsnmp-functions.md) that simplify management of the retransmission policy.</span></span>

<span data-ttu-id="776d5-117">À tout moment pendant l’exécution du programme, l’application WinSNMP peut ajuster l’exécution de la stratégie en effectuant l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="776d5-117">At any time during program execution, the WinSNMP application can adjust execution of the policy by performing one of the following steps:</span></span>

-   <span data-ttu-id="776d5-118">Demandez que l’implémentation démarre ou arrête l’exécution de la stratégie de retransmission en appelant la fonction [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="776d5-118">Request that the implementation start or stop executing the retransmission policy by calling the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="776d5-119">Pour plus d’informations, consultez [activation et désactivation de la retransmission](turning-retransmission-on-and-off.md).</span><span class="sxs-lookup"><span data-stu-id="776d5-119">For more information, see [Turning Retransmission On and Off](turning-retransmission-on-and-off.md).</span></span>
-   <span data-ttu-id="776d5-120">Modifiez les valeurs de délai d’attente et de nombre de nouvelles tentatives dans la base de données de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="776d5-120">Modify the time-out period and retry count values in the implementation's database.</span></span> <span data-ttu-id="776d5-121">Pour plus d’informations, consultez [modification de la stratégie de retransmission](changing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="776d5-121">For more information, see [Changing the Retransmission Policy](changing-the-retransmission-policy.md).</span></span>
-   <span data-ttu-id="776d5-122">Appelez la fonction [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) pour annuler le cycle de retransmission et libérer les structures de données internes associées à une demande de message SNMP unique.</span><span class="sxs-lookup"><span data-stu-id="776d5-122">Call the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function to cancel the retransmission cycle and release internal data structures associated with a single SNMP message request.</span></span> <span data-ttu-id="776d5-123">Pour plus d’informations, consultez annulation de la [retransmission](canceling-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="776d5-123">For more information, see [Canceling Retransmission](canceling-retransmission.md).</span></span>

<span data-ttu-id="776d5-124">L’application peut exécuter sa propre stratégie de retransmission.</span><span class="sxs-lookup"><span data-stu-id="776d5-124">The application can execute its own retransmission policy.</span></span> <span data-ttu-id="776d5-125">Dans ce cas, l’exécution peut ou non reposer sur les valeurs de la base de données.</span><span class="sxs-lookup"><span data-stu-id="776d5-125">In this case, execution may or may not be based on the values in the database.</span></span>

 

 




