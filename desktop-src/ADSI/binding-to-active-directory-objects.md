---
title: Liaison à des objets Active Directory
description: Avant de poursuivre ce scénario, vous devez comprendre comment les objets ADSI sont nommés dans Active Directory, et comment les lier. La liaison d’un objet ADSI connecte l’objet au service d’annuaire et vous permet d’accéder aux méthodes de l’objet.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028569"
---
# <a name="binding-to-active-directory-objects"></a><span data-ttu-id="f7f2e-104">Liaison à des objets Active Directory</span><span class="sxs-lookup"><span data-stu-id="f7f2e-104">Binding to Active Directory Objects</span></span>

<span data-ttu-id="f7f2e-105">Avant de poursuivre ce scénario, vous devez comprendre comment les objets ADSI sont nommés dans Active Directory, et comment les lier.</span><span class="sxs-lookup"><span data-stu-id="f7f2e-105">Before you continue with this scenario, you must understand how ADSI objects are named in Active Directory, and how to bind them.</span></span> <span data-ttu-id="f7f2e-106">La liaison d’un objet ADSI connecte l’objet au service d’annuaire et vous permet d’accéder aux méthodes de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f7f2e-106">Binding an ADSI object connects the object with the directory service, and allows you to access the methods of the object.</span></span>

## <a name="adspath"></a><span data-ttu-id="f7f2e-107">ADsPath</span><span class="sxs-lookup"><span data-stu-id="f7f2e-107">ADsPath</span></span>

<span data-ttu-id="f7f2e-108">Un objet ADSI est identifié de manière unique par sa chaîne de liaison, également appelée ADsPath.</span><span class="sxs-lookup"><span data-stu-id="f7f2e-108">An ADSI object is uniquely identified by its binding string, which is also referred to as an ADsPath.</span></span> <span data-ttu-id="f7f2e-109">Un ADsPath est une combinaison d’un identificateur programmatique (progID) du fournisseur ADSI et du nom unique (DN) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f7f2e-109">An ADsPath is a combination of a programmatic identifier (progID) of the ADSI provider, and the distinguished name (DN) of the object.</span></span>

<span data-ttu-id="f7f2e-110">Voici le format d’une ADsPath :</span><span class="sxs-lookup"><span data-stu-id="f7f2e-110">Here's the format of an ADsPath:</span></span>

<span data-ttu-id="f7f2e-111">« progID://DN »</span><span class="sxs-lookup"><span data-stu-id="f7f2e-111">"progID://DN"</span></span>

-   <span data-ttu-id="f7f2e-112">pogID : identificateur programmatique du fournisseur ADSI, tel que LDAP ou Winnt.</span><span class="sxs-lookup"><span data-stu-id="f7f2e-112">pogID — the programmatic identifier of the ADSI provider, such as LDAP or WinNT.</span></span>

-   <span data-ttu-id="f7f2e-113">:// : sépare le progID du DN.</span><span class="sxs-lookup"><span data-stu-id="f7f2e-113">:// — separates the progID from the DN.</span></span>

-   <span data-ttu-id="f7f2e-114">DN : nom unique de l’objet ADSI, qui est le chemin d’accès complet de l’objet, où le chemin d’accès se compose de noms uniques relatifs (RDN).</span><span class="sxs-lookup"><span data-stu-id="f7f2e-114">DN — the distinguished name of the ADSI object, which is the full path of the object, where the path consists of relative distinguished names (RDNs).</span></span>

<span data-ttu-id="f7f2e-115">Un RDN est le nom de l’objet sans le chemin d’accès et est unique à partir de ses objets frères.</span><span class="sxs-lookup"><span data-stu-id="f7f2e-115">An RDN is the name of the object without the path, and is unique from its sibling objects.</span></span> <span data-ttu-id="f7f2e-116">Un RDN se compose d’un ID d’attribut et d’une valeur, tels que « DC = fabrikam », où DC est l’attribut, et Fabrikam la valeur.</span><span class="sxs-lookup"><span data-stu-id="f7f2e-116">An RDN consists of an attribute ID and value, such as "DC=Fabrikam", where DC is the attribute, and Fabrikam is the value.</span></span> <span data-ttu-id="f7f2e-117">DC est un ID d’attribut RDN qui représente le composant de domaine.</span><span class="sxs-lookup"><span data-stu-id="f7f2e-117">DC is an RDN attribute ID that stands for domain component.</span></span>

<span data-ttu-id="f7f2e-118">Voici un exemple d’ADsPath :</span><span class="sxs-lookup"><span data-stu-id="f7f2e-118">Here’s an example of an ADsPath:</span></span>

<span data-ttu-id="f7f2e-119">« LDAP://DC = fabrikam, DC = com »</span><span class="sxs-lookup"><span data-stu-id="f7f2e-119">"LDAP://DC=Fabrikam,DC=Com"</span></span>

## <a name="binding-the-object"></a><span data-ttu-id="f7f2e-120">Liaison de l’objet</span><span class="sxs-lookup"><span data-stu-id="f7f2e-120">Binding the object</span></span>

<span data-ttu-id="f7f2e-121">Voici comment vous pouvez lier l’objet de domaine dans ce scénario :</span><span class="sxs-lookup"><span data-stu-id="f7f2e-121">Here's how you can bind the domain object in this scenario:</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



<span data-ttu-id="f7f2e-122">Lorsque vous exécutez cet exemple de code, ADSI utilise le DN pour déterminer les objets ADSI à lier.</span><span class="sxs-lookup"><span data-stu-id="f7f2e-122">When you run this code example, ADSI uses the DN to determine the ADSI objects to bind.</span></span> <span data-ttu-id="f7f2e-123">Une fois que l’interface ADSI a lié ces objets, vous pouvez accéder à leurs méthodes.</span><span class="sxs-lookup"><span data-stu-id="f7f2e-123">After ADSI binds these objects, you can access their methods.</span></span> <span data-ttu-id="f7f2e-124">L’exemple de code précédent lie un objet de domaine à [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) et [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span><span class="sxs-lookup"><span data-stu-id="f7f2e-124">The previous code example binds a domain object to [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="f7f2e-125">Vous pouvez maintenant utiliser des méthodes sur ces interfaces, telles que l' [**extraction**](/windows/desktop/api/Iads/nf-iads-iads-get), la [**mise en place**](/windows/desktop/api/Iads/nf-iads-iads-put), la [**création**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), la [**suppression**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)et l' [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span><span class="sxs-lookup"><span data-stu-id="f7f2e-125">You can now use methods on those interfaces such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete), and [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span></span>

<span data-ttu-id="f7f2e-126">Une fois que vous avez lié un objet de domaine, vous pouvez imprimer certains de ses attributs :</span><span class="sxs-lookup"><span data-stu-id="f7f2e-126">After you bind a domain object, you can print some of its attributes:</span></span>


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



<span data-ttu-id="f7f2e-127">Pour plus d’informations sur ADsPath, consultez [Binding String](binding-string.md).</span><span class="sxs-lookup"><span data-stu-id="f7f2e-127">For more information about ADsPath, see [Binding String](binding-string.md).</span></span> <span data-ttu-id="f7f2e-128">Pour plus d’informations sur la liaison, consultez [liaison à un objet ADSI](binding-to-an-adsi-object.md).</span><span class="sxs-lookup"><span data-stu-id="f7f2e-128">For more information about binding, see [Binding to an ADSI Object](binding-to-an-adsi-object.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7f2e-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7f2e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7f2e-130">Création d'une unité d'organisation</span><span class="sxs-lookup"><span data-stu-id="f7f2e-130">Creating an Organizational Unit</span></span>](creating-an-organizational-unit.md)
</dt> </dl>

 

 




