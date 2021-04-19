---
description: Le moniker de la file d’attente est utilisé pour activer un composant mis en file d’attente par programmation.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Utilisation du moniker de la file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228964157d08aca868474167ae16590692f16ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517407"
---
# <a name="using-the-queue-moniker"></a><span data-ttu-id="fc6ea-103">Utilisation du moniker de la file d’attente</span><span class="sxs-lookup"><span data-stu-id="fc6ea-103">Using the Queue Moniker</span></span>

<span data-ttu-id="fc6ea-104">Le moniker de la file d’attente est utilisé pour activer un composant mis en file d’attente par programmation.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-104">The queue moniker is used to activate a queued component programmatically.</span></span> <span data-ttu-id="fc6ea-105">Le moniker de la file d’attente requiert qu’il reçoive l’ID de classe (CLSID) de l’objet à appeler à partir du nouveau moniker directement à sa droite.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-105">The queue moniker requires that it receive the class ID (CLSID) of the object to be invoked from the new moniker directly to the right of it.</span></span> <span data-ttu-id="fc6ea-106">Lorsqu’il est préfixé à gauche, le nouveau moniker passe le CLSID au moniker à gauche de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-106">When left-prefixed, the new moniker passes the CLSID to the moniker to the left of it.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="fc6ea-107">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="fc6ea-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="fc6ea-108">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="fc6ea-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fc6ea-109">Visual Basic</span></span>

<span data-ttu-id="fc6ea-110">Le paramètre de nom complet GetObject est « queue:/New : », suivi de l’ID de programme ou du GUID de forme chaîne, avec ou sans accolades, de l’objet serveur à instancier.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-110">The GetObject display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="fc6ea-111">Les exemples suivants illustrent trois activations valides d’un composant avec le moniker de file d’attente :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-111">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a><span data-ttu-id="fc6ea-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="fc6ea-112">C/C++</span></span>

<span data-ttu-id="fc6ea-113">Le paramètre [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) Display Name est « queue:/New : », suivi de l’ID de programme ou du GUID de forme chaîne, avec ou sans accolades, de l’objet serveur à instancier.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-113">The [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="fc6ea-114">Les exemples suivants illustrent trois activations valides d’un composant avec le moniker de file d’attente :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-114">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:QCShip.Ship",
      NULL, IID_IShip, (void**)&pShip);
    ```

2.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}", 
      NULL, IID_IShip, (void**)&pShip);
    ```

3.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE",
      NULL, IID_IShip, (void**)&pShip);
    ```

## <a name="remarks"></a><span data-ttu-id="fc6ea-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fc6ea-115">Remarks</span></span>

<span data-ttu-id="fc6ea-116">Le moniker de la file d’attente accepte des paramètres facultatifs qui modifient les propriétés du message envoyé à Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-116">The queue moniker accepts optional parameters that alter the properties of the message sent to Message Queuing.</span></span> <span data-ttu-id="fc6ea-117">Par exemple, pour faire en sorte que le message Message Queuing soit envoyé avec une priorité 6, le composant mis en file d’attente est activé comme suit :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-117">For example, to cause the Message Queuing message to be sent with a priority 6, the queued component would be activated as follows:</span></span>

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

<span data-ttu-id="fc6ea-118">Le tableau suivant répertorie les paramètres du moniker de la file d’attente qui affectent la file d’attente de destination.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-118">The following table lists the queue moniker parameters that affect the destination queue.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc6ea-119">Paramètre</span><span class="sxs-lookup"><span data-stu-id="fc6ea-119">Parameter</span></span></th>
<th><span data-ttu-id="fc6ea-120">Description</span><span class="sxs-lookup"><span data-stu-id="fc6ea-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc6ea-121"><em>ComputerName</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-121"><em>ComputerName</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-122">Spécifie la partie nom d’ordinateur d’un nom de chemin d’accès de file d’attente Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-122">Specifies the computer name portion of a Message Queuing queue path name.</span></span> <span data-ttu-id="fc6ea-123">Le nom du chemin d’accès de la file d’attente Message Queuing est au format <em>ComputerName</em> \ <em>QueueName</em>.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-123">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="fc6ea-124">S’il n’est pas spécifié, le nom de l’ordinateur associé à l’application configurée est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-124">If not specified, the computer name associated with the configured application is used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc6ea-125"><em>QueueName</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-125"><em>QueueName</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-126">Spécifie le nom de la file d’attente Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-126">Specifies the Message Queuing queue name.</span></span> <span data-ttu-id="fc6ea-127">Le nom du chemin d’accès de la file d’attente Message Queuing est au format <em>ComputerName</em> \ <em>QueueName</em>.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-127">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="fc6ea-128">S’il n’est pas spécifié, le nom de la file d’attente associé à l’application configurée est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-128">If not specified, the queue name associated with the configured application is used.</span></span><br/> <span data-ttu-id="fc6ea-129">Pour obtenir une file d’attente non transactionnelle, vous pouvez d’abord spécifier le nom de la file d’attente, puis créer une application COM+ portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-129">To get a non-transactional queue, you can specify the queue name first and then create a COM+ application of the same name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc6ea-130"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-130"><em>PathName</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-131">Spécifie le nom complet du chemin d’accès de la file d’attente Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-131">Specifies the complete Message Queuing queue path name.</span></span> <span data-ttu-id="fc6ea-132">S’il n’est pas spécifié, le nom du chemin d’accès de la file d’attente Message Queuing associé à l’application configurée est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-132">If not specified, the Message Queuing queue path name associated with the configured application is used.</span></span> <span data-ttu-id="fc6ea-133">Pour remplacer le nom de destination, le chemin d’accès peut être spécifié sous la forme suivante pour une installation de Message Queuing groupe de travail :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-133">To override the destination name, the path can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="fc6ea-134">Queue :<em>pathname</em> = <em>nomordinateur</em>\private $ \ AppName/New : MyProject. CMyClass</span><span class="sxs-lookup"><span data-stu-id="fc6ea-134">Queue:<em>PathName</em>=<em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fc6ea-135">Les langages de programmation C et Microsoft Visual C++ requièrent deux barres obliques inverses pour représenter une barre oblique inverse dans les littéraux de chaîne, par exemple, Chicago \\ Payroll.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-135">Both the C and Microsoft Visual C++ programming languages require two backslashes to represent one backslash within string literals for example, chicago\\payroll.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc6ea-136"><em>FormatName</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-136"><em>FormatName</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-137">Lorsque vous marquez une application COM+ comme en file d’attente, COM+ crée une file d’attente Message Queuing dont le nom est identique à celui de l’application.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-137">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="fc6ea-138">Le nom de format Message Queuing de cette file d’attente se trouve dans le catalogue COM+, associé à l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-138">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="fc6ea-139">Pour remplacer le nom de destination, le nom de format peut être spécifié sous la forme suivante pour une installation Message Queuing groupe de travail :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-139">To override the destination name, the format name can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="fc6ea-140">Queue :<em>FormatName</em>= direct = OS :<em>nom_ordinateur</em>\private $ \ AppName/New : ProgID</span><span class="sxs-lookup"><span data-stu-id="fc6ea-140">Queue:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId</span></span><br/> <span data-ttu-id="fc6ea-141">Dans une configuration Active Directory, &quot; Private $ &quot; n’est pas spécifié dans le nom de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-141">In an Active Directory configuration, &quot;PRIVATE$&quot; is not specified as part of the queue name.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="fc6ea-142">Les paramètres facultatifs du moniker de la file d’attente sont traités de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-142">Optional queue moniker parameters are processed left-to-right.</span></span> <span data-ttu-id="fc6ea-143">Spécifiez chaque mot clé une seule fois.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-143">Specify each keyword only one time.</span></span> <span data-ttu-id="fc6ea-144">La spécification du paramètre *pathname* remplace les paramètres *ComputerName* et *QueueName*.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-144">Specifying the *PathName* parameter replaces both the *ComputerName* and *QueueName* parameters.</span></span> <span data-ttu-id="fc6ea-145">Un paramètre *FormatName* spécifique supprime la connaissance préalable d’un paramètre *ComputerName*, *QueueName* et *pathname* .</span><span class="sxs-lookup"><span data-stu-id="fc6ea-145">A specific *FormatName* parameter deletes prior knowledge of a *ComputerName*, *QueueName*, and *PathName* parameter.</span></span>

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a><span data-ttu-id="fc6ea-146">Association de l’écouteur de composants en file d’attente à une file d’attente privée spécifique</span><span class="sxs-lookup"><span data-stu-id="fc6ea-146">Associating the Queued Components Listener with a Specific Private Queue</span></span>

<span data-ttu-id="fc6ea-147">L’écouteur de composants en file d’attente COM+ reçoit uniquement des files d’attente associées à l’application COM+ marquée en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-147">The COM+ Queued Components listener receives only from queues associated with the COM+ application marked queued.</span></span> <span data-ttu-id="fc6ea-148">Lorsque vous marquez une application COM+ comme en file d’attente, COM+ crée une file d’attente Message Queuing dont le nom est identique à celui de l’application.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-148">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="fc6ea-149">Le nom de format Message Queuing de cette file d’attente se trouve dans le catalogue COM+, associé à l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-149">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="fc6ea-150">Lorsque l’application COM+ est démarrée et marquée comme Listen, un écouteur dans le processus de l’application COM+ est démarré et la file d’attente est ouverte.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-150">When the COM+ application is started and marked as listen, a listener in the COM+ application process is started and the queue is opened.</span></span> <span data-ttu-id="fc6ea-151">Le tableau suivant répertorie les paramètres du moniker de la file d’attente qui affectent le message de Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-151">The following table lists the queue moniker parameters that affect the Message Queuing message.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc6ea-152">Paramètre</span><span class="sxs-lookup"><span data-stu-id="fc6ea-152">Parameter</span></span></th>
<th><span data-ttu-id="fc6ea-153">Description</span><span class="sxs-lookup"><span data-stu-id="fc6ea-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc6ea-154"><em>AppSpecific</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-154"><em>AppSpecific</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-155">Spécifie un entier non signé, par exemple, AppSpecific = 12345.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-155">Specifies an unsigned integer for example, AppSpecific=12345.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc6ea-156"><em>AuthLevel</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-156"><em>AuthLevel</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-157">Spécifie le niveau d’authentification du message.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-157">Specifies the message authentication level.</span></span> <span data-ttu-id="fc6ea-158">Un message authentifié est signé numériquement et requiert un certificat pour l’utilisateur qui envoie le message.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-158">An authenticated message is digitally signed and requires a certificate for the user sending the message.</span></span> <span data-ttu-id="fc6ea-159">Valeurs acceptables :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-159">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="fc6ea-160">MQMSG_AUTH_LEVEL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="fc6ea-160">MQMSG_AUTH_LEVEL_NONE,0</span></span></li>
<li><span data-ttu-id="fc6ea-161">MQMSG_AUTH_LEVEL_ALWAYS, 1</span><span class="sxs-lookup"><span data-stu-id="fc6ea-161">MQMSG_AUTH_LEVEL_ALWAYS,1</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc6ea-162"><em>Distribution</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-162"><em>Delivery</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-163">Spécifie l’option de remise de message.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-163">Specifies the message delivery option.</span></span> <span data-ttu-id="fc6ea-164">Cette valeur est ignorée pour les files d’attente transactionnelles.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-164">This value is ignored for transactional queues.</span></span> <span data-ttu-id="fc6ea-165">Valeurs acceptables :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-165">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="fc6ea-166">MQMSG_DELIVERY_EXPRESS, 0</span><span class="sxs-lookup"><span data-stu-id="fc6ea-166">MQMSG_DELIVERY_EXPRESS,0</span></span></li>
<li><span data-ttu-id="fc6ea-167">MQMSG_DELIVERY_RECOVERABLE, 1</span><span class="sxs-lookup"><span data-stu-id="fc6ea-167">MQMSG_DELIVERY_RECOVERABLE,1</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc6ea-168"><em>EncryptAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-168"><em>EncryptAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-169">Spécifie l’algorithme de chiffrement à utiliser par Message Queuing pour chiffrer et déchiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-169">Specifies the encryption algorithm to be used by Message Queuing to encrypt and decrypt the message.</span></span> <span data-ttu-id="fc6ea-170">Valeurs acceptables :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-170">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="fc6ea-171">CALG_RC2, CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="fc6ea-171">CALG_RC2, CALG_RC4</span></span></li>
<li><span data-ttu-id="fc6ea-172">Toute valeur entière acceptable pour Message Queuing pour un <em>EncryptAlgorithm</em>.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-172">Any integer value that is acceptable to Message Queuing for an <em>EncryptAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc6ea-173"><em>HashAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-173"><em>HashAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-174">Spécifie une fonction de hachage de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-174">Specifies a cryptographic hash function.</span></span> <span data-ttu-id="fc6ea-175">Valeurs acceptables :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-175">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="fc6ea-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="fc6ea-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span></span></li>
<li><span data-ttu-id="fc6ea-177">Toute valeur entière acceptable pour Message Queuing pour un <em>HashAlgorithm</em>.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-177">Any integer value that is acceptable to Message Queuing for a <em>HashAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc6ea-178">Journal</span><span class="sxs-lookup"><span data-stu-id="fc6ea-178">Journal</span></span><br/></td>
<td><span data-ttu-id="fc6ea-179">Spécifie l’option Message Queuing le journal des messages.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-179">Specifies the Message Queuing message journal option.</span></span> <span data-ttu-id="fc6ea-180">Valeurs acceptables :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-180">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="fc6ea-181">MQMSG_JOURNAL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="fc6ea-181">MQMSG_JOURNAL_NONE,0</span></span></li>
<li><span data-ttu-id="fc6ea-182">MQMSG_DEADLETTER, 1</span><span class="sxs-lookup"><span data-stu-id="fc6ea-182">MQMSG_DEADLETTER,1</span></span></li>
<li><span data-ttu-id="fc6ea-183">MQMSG_JOURNAL, 2</span><span class="sxs-lookup"><span data-stu-id="fc6ea-183">MQMSG_JOURNAL,2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc6ea-184"><em>Étiquette</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-184"><em>Label</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-185">Spécifie une chaîne d’étiquette de message jusqu’à MQ_MAX_MSG_LABEL_LEN caractères.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-185">Specifies a message label string up to MQ_MAX_MSG_LABEL_LEN characters.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc6ea-186"><em>MaxTimeToReachQueue</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-186"><em>MaxTimeToReachQueue</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-187">Spécifie la durée maximale, en secondes, pendant laquelle le message atteint la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-187">Specifies a maximum time, in seconds, for the message to reach the queue.</span></span> <br/> <span data-ttu-id="fc6ea-188">Valeurs acceptables :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-188">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="fc6ea-189">INFINITE</span><span class="sxs-lookup"><span data-stu-id="fc6ea-189">INFINITE</span></span></li>
<li><span data-ttu-id="fc6ea-190">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="fc6ea-190">LONG_LIVED</span></span></li>
<li><span data-ttu-id="fc6ea-191">Nombre de secondes</span><span class="sxs-lookup"><span data-stu-id="fc6ea-191">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc6ea-192"><em>MaxTimeToReceive</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-192"><em>MaxTimeToReceive</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-193">Spécifie la durée maximale, en secondes, pendant laquelle le message est reçu par l’application cible.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-193">Specifies a maximum time, in seconds, for the message to be received by the target application.</span></span> <span data-ttu-id="fc6ea-194">Valeurs acceptables :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-194">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="fc6ea-195">INFINITE</span><span class="sxs-lookup"><span data-stu-id="fc6ea-195">INFINITE</span></span></li>
<li><span data-ttu-id="fc6ea-196">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="fc6ea-196">LONG_LIVED</span></span></li>
<li><span data-ttu-id="fc6ea-197">Nombre de secondes</span><span class="sxs-lookup"><span data-stu-id="fc6ea-197">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc6ea-198"><em>Priorité</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-198"><em>Priority</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-199">Spécifie un niveau de priorité de message dans les valeurs Message Queuing autorisées.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-199">Specifies a message priority level, within the Message Queuing values permitted.</span></span><br/> <span data-ttu-id="fc6ea-200">Valeurs acceptables :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-200">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="fc6ea-201">MQ_MIN_PRIORITY, 0</span><span class="sxs-lookup"><span data-stu-id="fc6ea-201">MQ_MIN_PRIORITY,0</span></span></li>
<li><span data-ttu-id="fc6ea-202">MQ_MAX_PRIORITY, 7</span><span class="sxs-lookup"><span data-stu-id="fc6ea-202">MQ_MAX_PRIORITY,7</span></span></li>
<li><span data-ttu-id="fc6ea-203">MQ_DEFAULT_PRIORITY, 3</span><span class="sxs-lookup"><span data-stu-id="fc6ea-203">MQ_DEFAULT_PRIORITY,3</span></span></li>
<li><span data-ttu-id="fc6ea-204">Nombre compris entre 0 et 7</span><span class="sxs-lookup"><span data-stu-id="fc6ea-204">Number between 0 and 7</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc6ea-205"><em>PrivLevel</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-205"><em>PrivLevel</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-206">Spécifie un niveau de confidentialité, utilisé pour chiffrer les messages.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-206">Specifies a privacy level, used to encrypt messages.</span></span><br/> <span data-ttu-id="fc6ea-207">Valeurs acceptables :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-207">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="fc6ea-208">MQMSG_PRIV_LEVEL_NONE, AUCUN, 0</span><span class="sxs-lookup"><span data-stu-id="fc6ea-208">MQMSG_PRIV_LEVEL_NONE, NONE, 0</span></span></li>
<li><span data-ttu-id="fc6ea-209">MQMSG_PRIV_LEVEL_BODY, CORPS,</span><span class="sxs-lookup"><span data-stu-id="fc6ea-209">MQMSG_PRIV_LEVEL_BODY, BODY,</span></span></li>
<li><span data-ttu-id="fc6ea-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span><span class="sxs-lookup"><span data-stu-id="fc6ea-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span></span></li>
<li><span data-ttu-id="fc6ea-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span><span class="sxs-lookup"><span data-stu-id="fc6ea-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc6ea-212"><em>Trace</em></span><span class="sxs-lookup"><span data-stu-id="fc6ea-212"><em>Trace</em></span></span><br/></td>
<td><span data-ttu-id="fc6ea-213">Spécifie les options de trace utilisées dans le suivi Message Queuing routage.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-213">Specifies trace options, used in tracing Message Queuing routing.</span></span><br/> <span data-ttu-id="fc6ea-214">Valeurs acceptables :</span><span class="sxs-lookup"><span data-stu-id="fc6ea-214">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="fc6ea-215">MQMSG_TRACE_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="fc6ea-215">MQMSG_TRACE_NONE,0</span></span></li>
<li><span data-ttu-id="fc6ea-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE, 1</span><span class="sxs-lookup"><span data-stu-id="fc6ea-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fc6ea-217">L’ensemble complet des fonctions du kit de développement logiciel (SDK) d’administration COM+ est disponible à l’aide d’objets COM.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-217">The complete set of COM+ Administrative SDK functions is available by using COM objects.</span></span> <span data-ttu-id="fc6ea-218">Cela permet à n’importe quel programme de démarrer et d’arrêter les applications COM+ selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-218">This allows any program to start and stop COM+ applications as required.</span></span>

> [!Note]  
> <span data-ttu-id="fc6ea-219">Lors du démarrage d’une application COM+, il s’agit de l’application en cours d’exécution, et non des composants individuels de l’application.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-219">When a COM+ application is started, it is the application that is running, not the individual components within the application.</span></span> <span data-ttu-id="fc6ea-220">Si une application appelle un composant non mis en file d’attente, l’application COM+ qui contient le composant est démarrée.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-220">If an application calls a non-queued component, the COM+ application that contains the component is started.</span></span> <span data-ttu-id="fc6ea-221">Si la case à cocher écouteur est activée, l’écouteur démarre et commence le traitement des messages pour les composants en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-221">If the listener check box is enabled, the listener also starts and begins processing for messages for queued components.</span></span> <span data-ttu-id="fc6ea-222">Alors que le service de composants en file d’attente peut être démarré de cette manière, si vous empaquetez des composants mis en file d’attente et non mis en file d’attente dans une seule application COM+, assurez-vous que vous souhaitez vraiment que les composants en file d’attente démarrent si un composant non mis en file d’attente est exécuté.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-222">While the queued components service can be started in this way, if you package queued and non-queued components into a single COM+ application, be sure that you really want queued components to start if a non-queued component is executed.</span></span> <span data-ttu-id="fc6ea-223">Si ce n’est pas le cas, empaquetez les composants mis en file d’attente dans une application COM+ distincte des autres composants.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-223">If this is not the case, package the queued components into a COM+ application that is separate from the other components.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fc6ea-224">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc6ea-224">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc6ea-225">Activation des files d’attente de composants</span><span class="sxs-lookup"><span data-stu-id="fc6ea-225">Activating Component Queues</span></span>](activating-component-queues.md)
</dt> </dl>

 

 




