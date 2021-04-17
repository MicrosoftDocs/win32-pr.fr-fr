---
title: notifier l’attribut
description: L’attribut \ Notify \ demande au compilateur MIDL de générer un appel à une procédure \ Notify \ du côté serveur de l’application.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- l’attribut de notification MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507531"
---
# <a name="notify-attribute"></a><span data-ttu-id="38683-104">notifier l’attribut</span><span class="sxs-lookup"><span data-stu-id="38683-104">notify attribute</span></span>

<span data-ttu-id="38683-105">L’attribut **\[ Notify \]** demande au compilateur MIDL de générer un appel à une procédure **\[ Notify \]** côté serveur de l’application.</span><span class="sxs-lookup"><span data-stu-id="38683-105">The **\[notify\]** attribute instructs the MIDL compiler to generate a call to a **\[notify\]** procedure on the server side of the application.</span></span>

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="38683-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38683-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38683-107">*nom de la procédure*</span><span class="sxs-lookup"><span data-stu-id="38683-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="38683-108">Nom de la procédure distante à laquelle la procédure Notify sera associée.</span><span class="sxs-lookup"><span data-stu-id="38683-108">The name of the remote procedure with which the notify procedure will be associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38683-109">Notes</span><span class="sxs-lookup"><span data-stu-id="38683-109">Remarks</span></span>

<span data-ttu-id="38683-110">La procédure **\[ Notify \]** appelée à la suite de l’attribut **\[ Notify \]** est associée à une procédure distante particulière sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="38683-110">The **\[notify\]** procedure called as a result of the **\[notify\]** attribute is associated with a particular remote procedure on the server.</span></span> <span data-ttu-id="38683-111">Son concept est similaire à une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="38683-111">It is similar in concept to a callback function.</span></span> <span data-ttu-id="38683-112">Le stub appelle la procédure **\[ Notify \]** après que tous les arguments de sortie de la procédure distante à laquelle il est associé ont été marshalés et que toute mémoire associée aux paramètres soit libérée.</span><span class="sxs-lookup"><span data-stu-id="38683-112">The stub calls the **\[notify\]** procedure after all the output arguments of the remote procedure with which it is associated have been marshaled and any memory associated with the parameters is freed.</span></span> <span data-ttu-id="38683-113">La routine **\[ Notify \]** est appelée si un appel échoue avant l’exécution de la routine de serveur.</span><span class="sxs-lookup"><span data-stu-id="38683-113">The **\[notify\]** routine is called if a call fails before the server routine executes.</span></span> <span data-ttu-id="38683-114">Par exemple, si un serveur échoue pendant le démarshaling en raison de la réception de données incorrectes du client, la \[ \] routine Notify est appelée.</span><span class="sxs-lookup"><span data-stu-id="38683-114">For example, if a server fails during unmarshaling due to receipt of bad data from the client, the \[notify\] routine is called.</span></span>

<span data-ttu-id="38683-115">L’attribut **\[ Notify \]** est utile pour développer des applications acquérant des ressources dans des procédures distantes.</span><span class="sxs-lookup"><span data-stu-id="38683-115">The **\[notify\]** attribute is useful to develop applications acquiring resources in remote procedures.</span></span> <span data-ttu-id="38683-116">Ces ressources sont ensuite libérées dans la procédure **\[ Notify \]** après que les paramètres de sortie de la procédure distante ont été entièrement marshalés.</span><span class="sxs-lookup"><span data-stu-id="38683-116">These resources are then freed in the **\[notify\]** procedure after the output parameters of the remote procedure are fully marshaled.</span></span>

<span data-ttu-id="38683-117">Le nom de la procédure **\[ Notify \]** est le nom de la procédure distante suffixée par **\_ Notify**.</span><span class="sxs-lookup"><span data-stu-id="38683-117">The **\[notify\]** procedure name is the name of the remote procedure suffixed by **\_notify**.</span></span> <span data-ttu-id="38683-118">La procédure **\_ Notify** ne nécessite aucun paramètre et ne retourne pas de résultat.</span><span class="sxs-lookup"><span data-stu-id="38683-118">The **\_notify** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="38683-119">Un prototype de cette procédure est également généré dans le fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="38683-119">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="38683-120">Par exemple, si le fichier IDL contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="38683-120">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="38683-121">Spécifiez ce qui suit dans le ACF pour MIDL pour générer l’appel de **\_ notification** :</span><span class="sxs-lookup"><span data-stu-id="38683-121">Specify the following in the ACF for MIDL to generate the **\_notify** call:</span></span>

``` syntax
[notify] MyProcedure();
```

<span data-ttu-id="38683-122">Le compilateur MIDL génère le code stub du serveur qui contient l’appel suivant à la procédure **\_ Notify** :</span><span class="sxs-lookup"><span data-stu-id="38683-122">The MIDL compiler will generate server stub code which contains the following call to the **\_notify** procedure:</span></span>

``` syntax
MyProcedure_notify();
```

<span data-ttu-id="38683-123">Le fichier d’en-tête contiendra un prototype :</span><span class="sxs-lookup"><span data-stu-id="38683-123">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a><span data-ttu-id="38683-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="38683-124">Examples</span></span>

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="38683-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38683-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38683-126">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="38683-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> </dl>

 

 




