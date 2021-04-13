---
description: Le LSA fournit plusieurs fonctions que les applications peuvent appeler pour énumérer ou définir des privilèges pour les comptes d’utilisateurs, de groupes et de groupes locaux.
ms.assetid: c28c03f0-4638-42ed-8dad-1e934cf99273
title: Gestion des autorisations de compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dc22a4088986abbdaa98d8cdde43415af84905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484585"
---
# <a name="managing-account-permissions"></a><span data-ttu-id="dca43-103">Gestion des autorisations de compte</span><span class="sxs-lookup"><span data-stu-id="dca43-103">Managing Account Permissions</span></span>

<span data-ttu-id="dca43-104">Le LSA fournit plusieurs fonctions que les applications peuvent appeler pour énumérer ou définir [*des privilèges*](/windows/desktop/SecGloss/p-gly) pour les comptes d’utilisateurs, de groupes et de groupes locaux.</span><span class="sxs-lookup"><span data-stu-id="dca43-104">The LSA provides several functions that applications can call to enumerate or set [*privileges*](/windows/desktop/SecGloss/p-gly) for user, group, and local group accounts.</span></span>

<span data-ttu-id="dca43-105">Avant de pouvoir gérer les informations de compte, votre application doit obtenir un descripteur de l’objet de [**stratégie**](policy-object.md) locale, comme indiqué dans [ouverture d’un handle d’objet de stratégie](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="dca43-105">Before you can manage account information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="dca43-106">En outre, pour énumérer ou modifier des autorisations pour un compte, vous devez disposer de l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) de ce compte.</span><span class="sxs-lookup"><span data-stu-id="dca43-106">In addition, to enumerate or edit permissions for an account, you must have the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) for that account.</span></span> <span data-ttu-id="dca43-107">Votre application peut localiser un SID en fonction du nom du compte, comme décrit dans [traduction entre les noms et les SID](translating-between-names-and-sids.md).</span><span class="sxs-lookup"><span data-stu-id="dca43-107">Your application can locate a SID given the account name, as described in [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>

<span data-ttu-id="dca43-108">Pour accéder à tous les comptes qui ont une autorisation particulière, appelez [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span><span class="sxs-lookup"><span data-stu-id="dca43-108">To access all accounts that have a particular permission, call [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span></span> <span data-ttu-id="dca43-109">Cette fonction remplit un tableau avec les SID de tous les comptes qui disposent de l’autorisation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dca43-109">This function populates an array with the SIDs of all accounts that have the specified permission.</span></span>

<span data-ttu-id="dca43-110">Une fois que vous avez obtenu le SID d’un compte, vous pouvez modifier ses autorisations.</span><span class="sxs-lookup"><span data-stu-id="dca43-110">After you have obtained the SID of an account, you can modify its permissions.</span></span> <span data-ttu-id="dca43-111">Appelez [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) pour ajouter des autorisations au compte.</span><span class="sxs-lookup"><span data-stu-id="dca43-111">Call [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) to add permissions to the account.</span></span> <span data-ttu-id="dca43-112">Si le compte spécifié n’existe pas, **LsaAddAccountRights** le crée.</span><span class="sxs-lookup"><span data-stu-id="dca43-112">If the specified account does not exist, **LsaAddAccountRights** creates it.</span></span> <span data-ttu-id="dca43-113">Pour supprimer des autorisations d’un compte, appelez [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span><span class="sxs-lookup"><span data-stu-id="dca43-113">To remove permissions from an account, call [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span></span> <span data-ttu-id="dca43-114">Si vous supprimez toutes les autorisations d’un compte, **LsaRemoveAccountRights** supprime également le compte.</span><span class="sxs-lookup"><span data-stu-id="dca43-114">If you remove all permissions from an account, **LsaRemoveAccountRights** also deletes the account.</span></span>

<span data-ttu-id="dca43-115">Votre application peut vérifier les autorisations actuellement affectées à un compte en appelant [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span><span class="sxs-lookup"><span data-stu-id="dca43-115">Your application can check the permissions currently assigned to an account by calling [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span></span> <span data-ttu-id="dca43-116">Cette fonction remplit un tableau de structures [**de \_ \_ chaînes Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="dca43-116">This function populates an array of [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structures.</span></span> <span data-ttu-id="dca43-117">Chaque structure contient le nom d’un privilège détenu par le compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="dca43-117">Each structure contains the name of a privilege held by the specified account.</span></span>

<span data-ttu-id="dca43-118">L’exemple suivant ajoute l’autorisation SeServiceLogonRight à un compte.</span><span class="sxs-lookup"><span data-stu-id="dca43-118">The following example adds the SeServiceLogonRight permission to an account.</span></span> <span data-ttu-id="dca43-119">Dans cet exemple, la variable AccountSID spécifie le SID du compte.</span><span class="sxs-lookup"><span data-stu-id="dca43-119">In this example, the AccountSID variable specifies the SID of the account.</span></span> <span data-ttu-id="dca43-120">Pour plus d’informations sur la recherche d’un SID de compte, consultez [conversion entre les noms et les SID](translating-between-names-and-sids.md).</span><span class="sxs-lookup"><span data-stu-id="dca43-120">For more information about how to lookup an account SID, see [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>


```C++
#include <windows.h>
#include <ntsecapi.h>

void AddPrivileges(PSID AccountSID, LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucPrivilege;
  NTSTATUS ntsResult;

  // Create an LSA_UNICODE_STRING for the privilege names.
  if (!InitLsaString(&lucPrivilege, L"SeServiceLogonRight"))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaAddAccountRights(
    PolicyHandle,  // An open policy handle.
    AccountSID,    // The target SID.
    &lucPrivilege, // The privileges.
    1              // Number of privileges.
  );                
  if (ntsResult == STATUS_SUCCESS) 
  {
    wprintf(L"Privilege added.\n");
  }
  else
  {
    wprintf(L"Privilege was not added - %lu \n",
      LsaNtStatusToWinError(ntsResult));
  }
} 
```



<span data-ttu-id="dca43-121">Dans l’exemple précédent, la fonction InitLsaString convertit une chaîne [*Unicode*](/windows/desktop/SecGloss/u-gly) en une structure de [**\_ \_ chaîne Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="dca43-121">In the preceding example, the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="dca43-122">Le code pour cette fonction s’affiche dans [utilisation de chaînes Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="dca43-122">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

 

 
