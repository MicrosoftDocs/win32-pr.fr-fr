---
title: Prise en charge de la liaison précoce
description: L’exemple de code suivant présente un scénario avec une prise en charge de la liaison précoce en place.
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- ADSI d’extensions, prise en charge de la liaison précoce
- liaison AD, prise en charge de la liaison précoce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102340"
---
# <a name="early-binding-support"></a><span data-ttu-id="661cd-105">Prise en charge de la liaison précoce</span><span class="sxs-lookup"><span data-stu-id="661cd-105">Early Binding Support</span></span>

<span data-ttu-id="661cd-106">L’exemple de code suivant présente un scénario avec une prise en charge de la liaison précoce en place.</span><span class="sxs-lookup"><span data-stu-id="661cd-106">The following code example presents a scenario with early binding support in place.</span></span>


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



<span data-ttu-id="661cd-107">Dans cet exemple de code, deux composants d’extension étendent un objet **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="661cd-107">In this code example, two extension components extend a **user** object.</span></span> <span data-ttu-id="661cd-108">Chaque extension publie sa propre interface.</span><span class="sxs-lookup"><span data-stu-id="661cd-108">Each extension publishes its own interface.</span></span> <span data-ttu-id="661cd-109">Chaque extension ne reconnaît pas l’autre interface d’extension ; seul ADSI reconnaît l’existence des deux extensions.</span><span class="sxs-lookup"><span data-stu-id="661cd-109">Each extension does not recognize the other extension interface; only ADSI recognizes the existence of both extensions.</span></span> <span data-ttu-id="661cd-110">Chaque extension délègue son [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) à ADSI.</span><span class="sxs-lookup"><span data-stu-id="661cd-110">Each extension delegates its [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to ADSI.</span></span> <span data-ttu-id="661cd-111">ADSI agit comme un agrégateur pour les deux extensions et toute autre extension future.</span><span class="sxs-lookup"><span data-stu-id="661cd-111">ADSI acts as an aggregator for both extensions, and any other future extensions.</span></span> <span data-ttu-id="661cd-112">L’interrogation d’une interface à partir de n’importe quelle extension, ou à partir d’ADSI, produit le même résultat cohérent.</span><span class="sxs-lookup"><span data-stu-id="661cd-112">Querying an interface from any extension, or from ADSI, yields the same consistent result.</span></span>

<span data-ttu-id="661cd-113">La procédure suivante décrit comment créer une extension.</span><span class="sxs-lookup"><span data-stu-id="661cd-113">The following procedure describes how to create an extension.</span></span>

## <a name="step-1-add-aggregation-to-your-component"></a><span data-ttu-id="661cd-114">Étape 1 : ajouter une agrégation à votre composant</span><span class="sxs-lookup"><span data-stu-id="661cd-114">Step 1: Add Aggregation to Your Component</span></span>

<span data-ttu-id="661cd-115">Suivez la spécification COM pour ajouter une agrégation à votre composant.</span><span class="sxs-lookup"><span data-stu-id="661cd-115">Follow the COM specification for adding aggregation to your component.</span></span> <span data-ttu-id="661cd-116">En résumé, vous devez accepter les demandes *pUnknown* à votre composant pendant **CreateInstance** et déléguer le *pUnknown* à l' [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’agrégateur si le composant est agrégé.</span><span class="sxs-lookup"><span data-stu-id="661cd-116">In summary, you must accept the *pUnknown* requests to your component during **CreateInstance**, and delegate the *pUnknown* to the aggregator's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) if the component is aggregated.</span></span>

## <a name="step-2-register-your-extension"></a><span data-ttu-id="661cd-117">Étape 2 : inscrire votre extension</span><span class="sxs-lookup"><span data-stu-id="661cd-117">Step 2: Register Your Extension</span></span>

<span data-ttu-id="661cd-118">Vous devez maintenant choisir la classe de répertoire à étendre.</span><span class="sxs-lookup"><span data-stu-id="661cd-118">Now you must decide which directory class to extend.</span></span> <span data-ttu-id="661cd-119">Vous ne pouvez pas utiliser les mêmes interfaces pour accomplir cela que vous utiliseriez pour une interface ADSI, par exemple [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span><span class="sxs-lookup"><span data-stu-id="661cd-119">You cannot use the same interfaces to accomplish this that you would use for an ADSI interface, for example, [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span></span> <span data-ttu-id="661cd-120">Les objets d’annuaire sont conservés dans l’annuaire, tandis que votre extension et ADSI s’exécutent sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="661cd-120">Directory objects are persisted in the directory, while your extension and ADSI are running on the client computer.</span></span> <span data-ttu-id="661cd-121">Les exemples d’objets d’annuaire sont **User**, **Computer**, **PrintQueue**, **serviceConnectionPoint** et **nTDSService**.</span><span class="sxs-lookup"><span data-stu-id="661cd-121">Directory object examples are **user**, **computer**, **printQueue**, **serviceConnectionPoint**, and **nTDSService**.</span></span> <span data-ttu-id="661cd-122">Vous pouvez ajouter une nouvelle classe dans Active Directory et créer également une nouvelle extension pour cette nouvelle classe.</span><span class="sxs-lookup"><span data-stu-id="661cd-122">You can add a new class in Active Directory and create a new extension for this new class as well.</span></span>

<span data-ttu-id="661cd-123">Vous utilisez des clés de Registre pour associer un nom de classe d’annuaire à des composants d’extension ADSI.</span><span class="sxs-lookup"><span data-stu-id="661cd-123">You use registry keys to associate a directory class name with the ADSI extension components.</span></span> <span data-ttu-id="661cd-124">La figure suivante représente la disposition de Registre existante, ainsi que de nouvelles clés.</span><span class="sxs-lookup"><span data-stu-id="661cd-124">The following figure represents the existing registry layout, as a well as new keys.</span></span>

-   <span data-ttu-id="661cd-125">Une nouvelle clé, appelée **Extensions**, contient une liste de clés, chacune représentant une classe dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="661cd-125">A new key, called **Extensions**, contains a list of keys, each of which represents a class in the directory.</span></span> <span data-ttu-id="661cd-126">Chaque classe, par exemple, **utilisateur**, **PrintQueue** ou **ordinateur**, gère une liste de sous-clés.</span><span class="sxs-lookup"><span data-stu-id="661cd-126">Each class, for example, **user**, **printQueue**, or **computer**, maintains a list of subkeys.</span></span>
-   <span data-ttu-id="661cd-127">Chaque sous-clé contient le CLSID du composant d’extension ADSI.</span><span class="sxs-lookup"><span data-stu-id="661cd-127">Each subkey contains the CLSID of the ADSI extension component.</span></span>
-   <span data-ttu-id="661cd-128">Chaque sous-clé CLSID contient une entrée de chaîne qui autorise plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="661cd-128">Each CLSID subkey contains a string entry that allows multiple values.</span></span> <span data-ttu-id="661cd-129">Vous devez uniquement répertorier les interfaces qui participent à l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="661cd-129">You should only list the interfaces that participate in the aggregation.</span></span>

> [!Note]  
> <span data-ttu-id="661cd-130">Les objets d’extension sont toujours requis pour enregistrer les clés COM standard.</span><span class="sxs-lookup"><span data-stu-id="661cd-130">Extension objects are still required to register standard COM keys.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a><span data-ttu-id="661cd-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="661cd-131">Example</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

<span data-ttu-id="661cd-132">La liste des interfaces de Extension1 peut être différente de celle de extension2.</span><span class="sxs-lookup"><span data-stu-id="661cd-132">The list of interfaces from Extension1 can be different from that of Extension2.</span></span> <span data-ttu-id="661cd-133">L’objet, lorsqu’il est actif, prend en charge les interfaces de l’agrégateur (ADSI) et toutes les interfaces fournies par les Extension1 et extension2 de l’agrégat.</span><span class="sxs-lookup"><span data-stu-id="661cd-133">The object, when active, supports the interfaces of the aggregator (ADSI) and all the interfaces provided by the aggregate's Extension1 and Extension2.</span></span> <span data-ttu-id="661cd-134">La résolution des interfaces en conflit (la même interface que celle prise en charge par l’agrégateur et les agrégats ou par plusieurs agrégats) est déterminée par les priorités des extensions.</span><span class="sxs-lookup"><span data-stu-id="661cd-134">Resolution of conflicting interfaces (the same interface supported by both the aggregator and the aggregates or by multiple aggregates) is determined by priorities of the extensions.</span></span>

<span data-ttu-id="661cd-135">Vous pouvez également associer votre extension CLSID à plusieurs noms de classes d’objets.</span><span class="sxs-lookup"><span data-stu-id="661cd-135">You can also associate your CLSID extension with multiple object class names.</span></span> <span data-ttu-id="661cd-136">Par exemple, votre extension peut étendre à la fois les objets **utilisateur** et **contact** .</span><span class="sxs-lookup"><span data-stu-id="661cd-136">For example, your extension can extend both the **user** and **contact** objects.</span></span>

> [!Note]  
> <span data-ttu-id="661cd-137">Le comportement d’extension est ajouté sur une classe par objet, et non sur une instance par objet.</span><span class="sxs-lookup"><span data-stu-id="661cd-137">Extension behavior is added on a per-object class, not on a per-object instance.</span></span>

 

<span data-ttu-id="661cd-138">Il est recommandé d’inscrire vos extensions, comme vous le feriez pour tout autre composant COM, avec un appel à la fonction **DllRegisterSvr** .</span><span class="sxs-lookup"><span data-stu-id="661cd-138">As a best practice, register your extensions, as you would any other COM components, with a call to the **DllRegisterSvr** function.</span></span> <span data-ttu-id="661cd-139">Fournissez également une fonctionnalité pour annuler l’inscription de votre extension avec la fonction **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="661cd-139">Also provide a facility to unregister your extension with the **DllUnregisterServer** function.</span></span>

<span data-ttu-id="661cd-140">L’exemple de code suivant montre comment inscrire une extension.</span><span class="sxs-lookup"><span data-stu-id="661cd-140">The following code example shows how to register an extension.</span></span>


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 