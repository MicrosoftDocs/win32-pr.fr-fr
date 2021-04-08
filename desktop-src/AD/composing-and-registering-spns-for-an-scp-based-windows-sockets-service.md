---
title: Composition et inscription de SPN pour le service Windows Sockets SCP
description: L’exemple de code suivant montre comment composer et inscrire les noms principaux de service (SPN) pour un service. Appelez ce code à partir de votre programme d’installation de service après avoir appelé CreateService et créé le point de connexion de service (SCP) du service.
ms.assetid: 3957af10-974a-415f-b8fb-d9b52ac5a82d
ms.tgt_platform: multiple
keywords:
- noms principaux de service Active Directory, composition et inscription de SPN pour un service Windows Sockets SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d754d51c0ad34b1623bdc84fc8178b04d33515ed
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724620"
---
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a><span data-ttu-id="34fec-105">Composition et inscription de SPN pour le service Windows Sockets SCP</span><span class="sxs-lookup"><span data-stu-id="34fec-105">Composing and registering SPNs for SCP-based Windows Sockets Service</span></span>

<span data-ttu-id="34fec-106">L’exemple de code suivant montre comment composer et inscrire les noms principaux de service (SPN) pour un service.</span><span class="sxs-lookup"><span data-stu-id="34fec-106">The following code example shows how to compose and register the SPNs for a service.</span></span> <span data-ttu-id="34fec-107">Appelez ce code à partir de votre programme d’installation de service après avoir appelé [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) et créé le point de connexion de service (SCP) du service.</span><span class="sxs-lookup"><span data-stu-id="34fec-107">Call this code from your service installer after calling [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) and creating the service's service connection point (SCP).</span></span>

<span data-ttu-id="34fec-108">L’exemple de code suivant appelle les fonctions d’exemple **SpnCompose** et **SpnRegister** qui composent et inscrivent le SPN.</span><span class="sxs-lookup"><span data-stu-id="34fec-108">The following code example calls the **SpnCompose** and **SpnRegister** example functions that compose and register the SPN.</span></span> <span data-ttu-id="34fec-109">Pour plus d’informations et le code source **SpnCompose** , consultez [composition des noms de principal du service pour un service avec SCP](composing-the-spns-for-a-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="34fec-109">For more information and the **SpnCompose** source code, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span> <span data-ttu-id="34fec-110">Pour plus d’informations et le code source **SpnRegister** , consultez [enregistrement des noms de principal du service pour un service](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="34fec-110">For more information and the **SpnRegister** source code, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

<span data-ttu-id="34fec-111">Cet exemple utilise le nom de la classe de service et le nom unique de son SCP pour créer son nom de principal du service.</span><span class="sxs-lookup"><span data-stu-id="34fec-111">This example uses the service class name and the distinguished name of its SCP to create its service principal name.</span></span> <span data-ttu-id="34fec-112">Pour plus d’informations et pour obtenir un exemple de code qui montre comment le client se lie au SCP du service pour récupérer ces chaînes de nom, consultez [Comment les clients recherchent et utilisent un point de connexion de service](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="34fec-112">For more information and a code example that shows how the client binds to the service SCP to retrieve these name strings, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="34fec-113">N’oubliez pas que le code pour composer un SPN varie selon le type de service et les mécanismes utilisés pour publier le service.</span><span class="sxs-lookup"><span data-stu-id="34fec-113">Be aware that the code for composing an SPN varies depending on the type of service and the mechanisms used to publish the service.</span></span>

<span data-ttu-id="34fec-114">Le service enregistre son SPN en le stockant dans l’attribut **servicePrincipalName** de l’objet de compte du service dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="34fec-114">The service registers its SPN by storing it in the **servicePrincipalName** attribute of the service's account object in the directory.</span></span> <span data-ttu-id="34fec-115">Si le service s’exécute sous le compte LocalSystem et non sous un compte de service, il inscrit son SPN sous l’objet du compte de l’ordinateur local dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="34fec-115">If the service runs under the LocalSystem account instead of under a service account, it registers its SPN under the local computer account's object in the directory.</span></span>


```C++
TCHAR szDNofSCP[MAX_PATH]; // DN of SCP. Initialize by querying SCP.
TCHAR szServiceClass[]=TEXT("ADSockAuth");
LPCTSTR szServiceAccountDN;   // DN of a service logon account. 
 
DWORD dwStatus;
TCHAR **pspn = NULL;
ULONG ulSpn = 1;
 
// Compose the SPNs.
dwStatus = SpnCompose(
        &pspn,              // Receives pointer to the SPN array.
        &ulSpn,             // Receives number of SPNs returned.
        szDNofSCP,          // Input: DN of the SCP.
        szServiceClass);    // Input: the service class string.
 
// Register the SPNs
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
       szServiceAccountDN,  // Logon account to register SPNs on
       pspn,                // Array of SPNs
       ulSpn,               // Number of SPNs in array
       DS_SPN_ADD_SPN_OP);  // Add SPNs to the account
 
// Free the array of SPNs returned by SpnCompose.
DsFreeSpnArray(ulSpn, pspn); 
```



<span data-ttu-id="34fec-116">Vous pouvez utiliser du code similaire pour annuler l’inscription de vos SPN lors de la désinstallation de votre service.</span><span class="sxs-lookup"><span data-stu-id="34fec-116">You can use similar code to unregister your SPNs when your service is uninstalled.</span></span> <span data-ttu-id="34fec-117">Spécifiez l’opération de suppression du SPN du service de nom principal de service DS au lieu du **\_ SPN DS \_ Ajouter le \_ SPN \_**. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="34fec-117">Specify the **DS\_SPN\_DELETE\_SPN\_OP** operation instead of **DS\_SPN\_ADD\_SPN\_OP**.</span></span>

 

 