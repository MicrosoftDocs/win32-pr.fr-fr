---
description: La stratégie LSA fournit deux fonctions que vous pouvez utiliser pour définir et récupérer des données privées.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Stockage des données privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6281f77e66a4217bda534b34342d6cefd92bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393499"
---
# <a name="storing-private-data"></a><span data-ttu-id="f3fe7-103">Stockage des données privées</span><span class="sxs-lookup"><span data-stu-id="f3fe7-103">Storing Private Data</span></span>

<span data-ttu-id="f3fe7-104">La stratégie LSA fournit deux fonctions que vous pouvez utiliser pour définir et récupérer des données privées.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-104">LSA Policy provides two functions that you can use to set and retrieve private data.</span></span> <span data-ttu-id="f3fe7-105">Ces données sont stockées sous la forme d’une chaîne chiffrée dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-105">This data is stored as an encrypted string in the registry.</span></span> <span data-ttu-id="f3fe7-106">Par exemple, vous pouvez utiliser ces fonctions pour stocker des mots de passe de compte de serveur et d’autres informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-106">For example, you can use these functions to store server account passwords and other sensitive information.</span></span>

<span data-ttu-id="f3fe7-107">Appelez la fonction [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) pour stocker et chiffrer les données privées.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-107">Call the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function to store and encrypt private data.</span></span> <span data-ttu-id="f3fe7-108">Comme décrit dans [objet de données privées](private-data-object.md), les objets de données privés incluent trois types spécialisés : local, global et machine.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-108">As described in [Private Data Object](private-data-object.md), private data objects include three specialized types: local, global, and machine.</span></span> <span data-ttu-id="f3fe7-109">Pour créer un objet spécialisé, ajoutez un préfixe au nom de clé passé à **LsaStorePrivateData**: « L $ » pour les objets locaux, « G $ » pour les objets globaux et « M $ » pour les objets ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-109">To create a specialized object, add a prefix to the key name passed to **LsaStorePrivateData**: "L$" for local objects, "G$" for global objects, and "M$" for machine objects.</span></span> <span data-ttu-id="f3fe7-110">Si vous ne créez pas l’un de ces types spécialisés, vous n’avez pas besoin de spécifier un préfixe de nom de clé.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-110">If you are not creating one of these specialized types, you do not need to specify a key name prefix.</span></span>

<span data-ttu-id="f3fe7-111">Pour récupérer et décoder des données privées précédemment stockées, appelez [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata).</span><span class="sxs-lookup"><span data-stu-id="f3fe7-111">To retrieve and decode previously stored private data, call [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata).</span></span> <span data-ttu-id="f3fe7-112">Notez que vous ne pouvez pas récupérer les objets de données privées de l’ordinateur ; les objets ordinateur ne peuvent être récupérés que par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-112">Note that you cannot retrieve machine private data objects; machine objects can be retrieved only by the operating system.</span></span>

<span data-ttu-id="f3fe7-113">Avant de pouvoir stocker ou récupérer des données privées, votre application doit obtenir un descripteur de l’objet de [**stratégie**](policy-object.md) local, comme indiqué dans [ouverture d’un handle d’objet de stratégie](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="f3fe7-113">Before you can store or retrieve private data, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="f3fe7-114">L’exemple suivant crée un objet de données privées locales.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-114">The following example creates a local private data object.</span></span> <span data-ttu-id="f3fe7-115">Notez que la fonction InitLsaString convertit une chaîne [*Unicode*](/windows/desktop/SecGloss/u-gly) en une structure de [**\_ \_ chaîne Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="f3fe7-115">Note that the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="f3fe7-116">Le code pour cette fonction s’affiche dans [utilisation de chaînes Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="f3fe7-116">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="f3fe7-117">Les données stockées par la fonction [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) ne sont pas entièrement protégées.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-117">The data stored by the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function is not absolutely protected.</span></span> <span data-ttu-id="f3fe7-118">Toutefois, la clé a une liste de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) qui permet uniquement au créateur et aux administrateurs de lire les données.</span><span class="sxs-lookup"><span data-stu-id="f3fe7-118">The key, however, has a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that allows only the creator and administrators to read the data.</span></span>

 

 

 
