---
description: Définit les paramètres d’entrée et de sortie des méthodes.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: Classe __PARAMETERS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527934"
---
# <a name="__parameters-class"></a><span data-ttu-id="0c1c5-103">\_\_Parameters, classe</span><span class="sxs-lookup"><span data-stu-id="0c1c5-103">\_\_PARAMETERS class</span></span>

<span data-ttu-id="0c1c5-104">La classe de système **\_ \_ Parameters** est une classe abstraite qui définit les paramètres d’entrée et de sortie des méthodes.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-104">The **\_\_PARAMETERS** system class is an abstract class that defines the input and output parameters for methods.</span></span> <span data-ttu-id="0c1c5-105">Il est également utilisé pour passer des valeurs de paramètre d’entrée et de sortie entre un client WMI et un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-105">It is also used to pass input and output parameter values between a WMI client and a method provider.</span></span>

<span data-ttu-id="0c1c5-106">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0c1c5-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c1c5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c1c5-108">Syntax</span></span>

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a><span data-ttu-id="0c1c5-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0c1c5-109">Members</span></span>

<span data-ttu-id="0c1c5-110">La classe **\_ \_ Parameters** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-110">The **\_\_PARAMETERS** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c1c5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0c1c5-111">Remarks</span></span>

<span data-ttu-id="0c1c5-112">Pour définir une méthode dans une classe d’utilisateur, un client WMI crée une copie de la classe de **\_ \_ paramètres** et ajoute une propriété pour chaque paramètre d’entrée dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-112">To define a method in a user class, a WMI client creates a copy of the **\_\_PARAMETERS** class, and adds a property for each input parameter in a method.</span></span> <span data-ttu-id="0c1c5-113">Si la méthode contient une valeur de retour ou des paramètres de sortie, une autre copie des **\_ \_ paramètres** doit être créée.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-113">If the method contains a return value or output parameters, another copy of **\_\_PARAMETERS** must be created.</span></span> <span data-ttu-id="0c1c5-114">Si la méthode retourne une valeur de retour, le client doit ajouter une propriété nommée **returnValue**.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-114">If the method returns a return value, the client must add a property named **ReturnValue**.</span></span> <span data-ttu-id="0c1c5-115">Le fournisseur de méthode stocke ensuite les paramètres de méthode avec un appel à [**IWbemClassObject ::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="0c1c5-115">The method provider then stores the method parameters with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="0c1c5-116">Pour appeler une méthode, un client appelle les éléments suivants dans l’ordre :</span><span class="sxs-lookup"><span data-stu-id="0c1c5-116">To invoke a method, a client calls the following in sequence:</span></span>

1.  <span data-ttu-id="0c1c5-117">[**IWbemClassObject :: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) pour récupérer une copie de la classe de **\_ \_ paramètres** qui est stockée par [**IWbemClassObject ::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="0c1c5-117">[**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve a copy of the **\_\_PARAMETERS** class that is stored by [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>
2.  <span data-ttu-id="0c1c5-118">[**IWbemClassObject :: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), puis définit une propriété pour chaque paramètre d’entrée de la méthode.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-118">[**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), and then sets one property for each input parameter to the method.</span></span>
3.  <span data-ttu-id="0c1c5-119">[**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) pour exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-119">[**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) to execute the method.</span></span>

<span data-ttu-id="0c1c5-120">Une fois l’exécution de la méthode terminée, une autre instance de la classe **\_ \_ Parameters** peut être retournée si la méthode a des paramètres de sortie ou une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-120">After the method is finished executing, another **\_\_PARAMETERS** class instance may be returned if the method has output parameters or a return value.</span></span>

-   <span data-ttu-id="0c1c5-121">Si la méthode a été appelée à l’aide de [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), l’instance des **\_ \_ paramètres** est retournée en tant qu’argument de sortie.</span><span class="sxs-lookup"><span data-stu-id="0c1c5-121">If the method was invoked by using [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), the **\_\_PARAMETERS** instance is returned as an output argument.</span></span>
-   <span data-ttu-id="0c1c5-122">Si la méthode a été appelée à l’aide de [**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), l’instance de **\_ \_ paramètres** est retournée en tant que paramètre à [**IWbemObjectSink :: indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span><span class="sxs-lookup"><span data-stu-id="0c1c5-122">If the method was invoked by using [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), the **\_\_PARAMETERS** instance is returned as a parameter to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c1c5-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c1c5-123">Requirements</span></span>



| <span data-ttu-id="0c1c5-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c1c5-124">Requirement</span></span> | <span data-ttu-id="0c1c5-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c1c5-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0c1c5-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c1c5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0c1c5-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c1c5-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0c1c5-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c1c5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0c1c5-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c1c5-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="0c1c5-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0c1c5-130">Namespace</span></span><br/>                | <span data-ttu-id="0c1c5-131">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="0c1c5-131">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="0c1c5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c1c5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c1c5-133">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="0c1c5-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="0c1c5-134">**IWbemServices :: ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="0c1c5-134">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="0c1c5-135">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="0c1c5-135">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 




