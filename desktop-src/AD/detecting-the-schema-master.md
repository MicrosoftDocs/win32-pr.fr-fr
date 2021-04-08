---
title: Détection du contrôleur de schéma
description: Active Directory Domain Services disposez d’un système de mise à jour multimaître ; chaque contrôleur de domaine contient une copie accessible en écriture de l’annuaire.
ms.assetid: 8e096351-43f8-48ee-acb6-681d9e38e93c
ms.tgt_platform: multiple
keywords:
- Détection de l’AD du contrôleur de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6869853cba68d7155f2091e2fe4515116944a629
ms.sourcegitcommit: f730b85cc85448913e50a7f331e10b646ea7978b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/23/2019
ms.locfileid: "103840934"
---
# <a name="detecting-the-schema-master"></a><span data-ttu-id="8ae9c-104">Détection du contrôleur de schéma</span><span class="sxs-lookup"><span data-stu-id="8ae9c-104">Detecting the Schema Master</span></span>

<span data-ttu-id="8ae9c-105">Active Directory Domain Services disposez d’un système de mise à jour multimaître ; chaque contrôleur de domaine contient une copie accessible en écriture de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-105">Active Directory Domain Services have a multi-master update system; every domain controller holds a writable copy of the directory.</span></span> <span data-ttu-id="8ae9c-106">Les mises à jour de schéma sont propagées à tous les domaines qui appartiennent à la même arborescence ou forêt.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-106">Schema updates are propagated to all domains that belong to the same tree or forest.</span></span> <span data-ttu-id="8ae9c-107">Étant donné qu’il est difficile de rapprocher les mises à jour conflictuelles du schéma, les mises à jour de schéma ne peuvent être effectuées que sur un seul serveur.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-107">Because it is difficult to reconcile conflicting updates to the schema, schema updates can only be performed at a single server.</span></span> <span data-ttu-id="8ae9c-108">Le serveur ayant le droit d’effectuer des mises à jour peut changer, mais un seul serveur aura ce droit à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-108">The server with the right to perform updates can change, but only one server will have that right at any given time.</span></span> <span data-ttu-id="8ae9c-109">Ce serveur est appelé le contrôleur de schéma.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-109">This server is called the schema master.</span></span> <span data-ttu-id="8ae9c-110">Le premier contrôleur de bus installé dans une entreprise est, par défaut, le contrôleur de schéma.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-110">The first DC installed in an enterprise is, by default, the schema master.</span></span>

<span data-ttu-id="8ae9c-111">Les modifications de schéma ne peuvent être effectuées qu’au niveau du contrôleur de schéma.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-111">Schema changes can only be made at the schema master level.</span></span> <span data-ttu-id="8ae9c-112">Pour détecter le contrôleur de bus de schéma, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-112">To detect which DC is the schema master, perform the following steps.</span></span>

<span data-ttu-id="8ae9c-113">**Détection du contrôleur de schéma DC**</span><span class="sxs-lookup"><span data-stu-id="8ae9c-113">**Detecting the DC Schema Master**</span></span>

1.  <span data-ttu-id="8ae9c-114">Lisez l’attribut **fSMORoleOwner** du conteneur de schéma sur n’importe quel contrôleur de périphérique.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-114">Read the **fsmoRoleOwner** attribute of the schema container on any DC.</span></span> <span data-ttu-id="8ae9c-115">L’attribut **fSMORoleOwner** retourne le nom unique (DN) de l’objet **nTDSDSA** pour le contrôleur de schéma.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-115">The **fsmoRoleOwner** attribute returns the distinguished name (DN) of the **nTDSDSA** object for the schema master.</span></span>
2.  <span data-ttu-id="8ae9c-116">Liez l’objet **nTDSDSA** dont vous venez de récupérer le nom unique.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-116">Bind to the **nTDSDSA** object whose DN you just retrieved.</span></span> <span data-ttu-id="8ae9c-117">Le parent de cet objet est l’objet serveur pour le contrôleur de bus contenant le contrôleur de schéma.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-117">The parent of this object is the server object for the DC containing the schema master.</span></span>
3.  <span data-ttu-id="8ae9c-118">Obtient l’ADsPath du parent de l’objet **nTDSDSA** .</span><span class="sxs-lookup"><span data-stu-id="8ae9c-118">Get the ADsPath for the parent of the **nTDSDSA** object.</span></span> <span data-ttu-id="8ae9c-119">Le parent est un objet serveur.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-119">The parent is a server object.</span></span>
4.  <span data-ttu-id="8ae9c-120">Lier à l’objet serveur.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-120">Bind to the server object.</span></span>
5.  <span data-ttu-id="8ae9c-121">Obtient l’attribut **dNSHostName** de l’objet serveur.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-121">Get the **dNSHostName** attribute of the server object.</span></span> <span data-ttu-id="8ae9c-122">Il s’agit du nom DNS du contrôleur de domaine qui contient le contrôleur de schéma.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-122">This is the DNS name of the DC that contains the schema master.</span></span>
6.  <span data-ttu-id="8ae9c-123">Spécifiez le nom DNS du contrôleur de schéma en tant que serveur et DN comme nom unique du conteneur de schéma à lier au contrôleur de schéma.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-123">Specify the DNS name of the schema master as the server and the DN as the DN of the schema container to bind to the schema master.</span></span> <span data-ttu-id="8ae9c-124">Par exemple, si le serveur était « dc1.fabrikam.com » et que le nom de domaine du conteneur de schéma était « CN = Schema, CN = Configuration, DC = fabrikam, DC = com », le chemin ADsPath serait le suivant.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-124">For example, if the server was "dc1.fabrikam.com" and the schema container DN was "cn=schema,cn=configuration,dc=fabrikam,dc=com", the ADsPath would be as follows.</span></span>
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

<span data-ttu-id="8ae9c-125">Il est recommandé de trouver le contrôleur de schéma et de vous y lier pour apporter des modifications au schéma.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-125">It is recommended that you find the schema master and bind to it to make schema changes.</span></span> <span data-ttu-id="8ae9c-126">Toutefois, vous pouvez déplacer le contrôleur de schéma vers un autre serveur.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-126">However, you can move the schema master to another server.</span></span>

<span data-ttu-id="8ae9c-127">Pour faire d’un autre serveur le contrôleur de schéma, un utilisateur convenablement privilégié peut effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ae9c-127">To make another server the schema master, a suitably privileged user can:</span></span>

-   <span data-ttu-id="8ae9c-128">Utilisez le composant logiciel enfichable MMC du gestionnaire de schémas.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-128">Use the Schema Manager MMC snap-in.</span></span>
    > [!Note]
    > <span data-ttu-id="8ae9c-129">Le composant logiciel enfichable MMC du schéma Active Directory doit être inscrit manuellement.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-129">The Active Directory Schema MMC snap-in must be registered manually.</span></span> <span data-ttu-id="8ae9c-130">Pour inscrire le composant logiciel enfichable Schéma, vous devez exécuter la commande suivante à partir de l’invite de commandes dans le répertoire system32 de Windows.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-130">To register the Schema snap-in, you must run the following command from the command prompt in the Windows System32 directory.</span></span>
    >
    > <span data-ttu-id="8ae9c-131">**regsvr32.exe schmmgmt.dll**</span><span class="sxs-lookup"><span data-stu-id="8ae9c-131">**regsvr32.exe schmmgmt.dll**</span></span>

     

-   <span data-ttu-id="8ae9c-132">Utilisez l’utilitaire de ligne de commande NTDSUTIL.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-132">Use the NTDSUTIL command-line utility.</span></span>
-   <span data-ttu-id="8ae9c-133">Utilisez une application tierce (une application qui émet l’écriture LDAP appropriée).</span><span class="sxs-lookup"><span data-stu-id="8ae9c-133">Use a third-party application (an application that issues the appropriate LDAP write).</span></span>

<span data-ttu-id="8ae9c-134">Pour devenir le contrôleur de schéma par programme, une application exécutée dans le contexte d’un utilisateur convenablement privilégié peut émettre une écriture LDAP de l’attribut opérationnel **becomeSchemaMaster** vers le RootDSE sur ce contrôleur de périphérique.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-134">To become the schema master programmatically, an application running in the context of a suitably privileged user can issue an LDAP write of the operational attribute **becomeSchemaMaster** to the rootDSE on that DC.</span></span> <span data-ttu-id="8ae9c-135">Cela lance un transfert atomique du contrôleur de schéma directement à partir du détenteur actuel vers le contrôleur de bus local.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-135">This initiates an atomic transfer of the schema master right from the current holder to the local DC.</span></span>

<span data-ttu-id="8ae9c-136">L’exemple de code suivant recherche le contrôleur de schéma.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-136">The following code example finds the schema master.</span></span> <span data-ttu-id="8ae9c-137">La fonction suivante est liée au conteneur de schéma sur l’ordinateur qui est le contrôleur de schéma.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-137">The following function binds to the schema container on the computer that is the schema master.</span></span>


```C++
HRESULT BindToSchemaMaster(IADsContainer **ppSchemaMaster)
{
HRESULT hr = E_FAIL;
// Get rootDSE and the schema container DN.
IADs *pObject = NULL;
IADs *pTempSchema = NULL;
IADs *pNTDS = NULL;
IADs *pServer = NULL;
BSTR bstrParent;
LPOLESTR szPath = new OLECHAR[MAX_PATH];
VARIANT var, varRole,varComputer;
hr = ADsOpenObject(L"LDAP://rootDSE",
         NULL,
         NULL,
         ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
         IID_IADs,
         (void**)&pObject);
if (hr == S_OK)
{
  hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
  if (hr == S_OK)
  {
    wcscpy_s(szPath,L"LDAP://");
    wcscat_s(szPath,var.bstrVal);
    hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
             IID_IADs,
             (void**)&pTempSchema);
 
    if (hr == S_OK)
    {
      /*
      Read the fsmoRoleOwner attribute to identify which server is 
      the schema master.
      */  
      hr = pTempSchema->Get(CComBSTR("fsmoRoleOwner"), &varRole);
      if (hr == S_OK)
      {
        // The fsmoRoleOwner attribute returns the nTDSDSA object.
        // The parent is the server object.
        // Bind to NTDSDSA object and get parent.
        wcscpy_s(szPath,L"LDAP://");
        wcscat_s(szPath,varRole.bstrVal);
        hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)&pNTDS);
        if (hr == S_OK)
        {
          hr = pNTDS->get_Parent(&bstrParent);
          if (hr == S_OK)
          {
            /*
            Bind to server object and get the DNS name of 
            the server.
            */
            wcscpy_s(szPath,bstrParent);
            hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION,
               IID_IADs,
               (void**)&pServer);
            if (hr == S_OK)
            {
              // Get the dns name of the server.
              hr = pServer->Get(CComBSTR("dNSHostName"), 
                  &varComputer);
              if (hr == S_OK)
              {
                    wcscpy_s(szPath,L"LDAP://");
                    wcscat_s(szPath,varComputer.bstrVal);
                    wcscat_s(szPath,L"/");
                    wcscat_s(szPath,var.bstrVal);
                    hr = ADsOpenObject(szPath,
                         NULL,
                         NULL,
                         ADS_SECURE_AUTHENTICATION,
                         IID_IADs,
                         (void**)ppSchemaMaster);
                    if (FAILED(hr))
                    {
                      if (*ppSchemaMaster)
                      {
                        (*ppSchemaMaster)->Release();
                        (*ppSchemaMaster) = NULL;
                      }
                    }
              }
              VariantClear(&varComputer);
            }
            if (pServer)
              pServer->Release();
          }
          SysFreeString(bstrParent);
        }
        if (pNTDS)
          pNTDS->Release();
      }
      VariantClear(&varRole);
    }
    if (pTempSchema)
      pTempSchema->Release();
  }
  VariantClear(&var);
}
if (pObject)
    pObject->Release();
 
return hr;
}
```



<span data-ttu-id="8ae9c-138">L’exemple de code suivant affiche le nom DNS de l’ordinateur qui est le contrôleur de schéma.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-138">The following code example displays the DNS name for the computer that is the schema master.</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
''''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the schema
''''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the schema container
''''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the 
' schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' The fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get the parent object.
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("dNSHostName")
''''''''''''''''''''
' Display the DNS name for the computer.
''''''''''''''''''''
strText = "Schema master has the following DNS name: "& sComputer
WScript.echo strText
 
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




