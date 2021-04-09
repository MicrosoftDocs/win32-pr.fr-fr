---
description: Une requête asynchrone, bien qu’un peu plus complexe à écrire, est le type de requête par défaut, lorsque les performances du système ou du réseau seront affectées par l’interrogation d’un grand groupe de données.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Appel d’une requête asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a0e297c6a1955d0006d888fc95f5e827f5cb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868746"
---
# <a name="invoking-an-asynchronous-query"></a><span data-ttu-id="cfed0-103">Appel d’une requête asynchrone</span><span class="sxs-lookup"><span data-stu-id="cfed0-103">Invoking an Asynchronous Query</span></span>

<span data-ttu-id="cfed0-104">Une requête asynchrone, bien qu’un peu plus complexe à écrire, est le type de requête par défaut, lorsque les performances du système ou du réseau seront affectées par l’interrogation d’un grand groupe de données.</span><span class="sxs-lookup"><span data-stu-id="cfed0-104">An asynchronous query, while somewhat more complex to write, is the preferred type of query when system or network performance will be affected by querying a large group of data.</span></span> <span data-ttu-id="cfed0-105">Dans le script, créer un objet [**SWbemSink**](swbemsink.md) et des sous-routines pour gérer les événements que le récepteur peut recevoir sont les seules tâches supplémentaires au-delà de la requête de base.</span><span class="sxs-lookup"><span data-stu-id="cfed0-105">In script, creating an [**SWbemSink**](swbemsink.md) object and subroutines to handle the events that the sink could receive are the only additional tasks beyond the basic query.</span></span>

> [!Note]  
> <span data-ttu-id="cfed0-106">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="cfed0-106">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="cfed0-107">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cfed0-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="cfed0-108">Les requêtes de script abrégées suivantes pour tous les fichiers de données sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="cfed0-108">The following abbreviated script queries for all of the data files on the local machine.</span></span> <span data-ttu-id="cfed0-109">Cette requête peut prendre beaucoup de temps si elle a été exécutée pour tous les ordinateurs d’un réseau.</span><span class="sxs-lookup"><span data-stu-id="cfed0-109">This query could take an excessive amount of time if it were executed for all of the machines on a network.</span></span> <span data-ttu-id="cfed0-110">Un objet [**SWbemSink**](swbemsink.md) est configuré et le seul événement géré est l’événement OnCompleted.</span><span class="sxs-lookup"><span data-stu-id="cfed0-110">An [**SWbemSink**](swbemsink.md) object is set up and the only event that is handled is the OnCompleted event.</span></span>


```VB
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
    WScript.Echo "Asynchronous operation is done."
End Sub

Set service = GetObject("winmgmts:")
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
service.ExecQueryAsync sink, "SELECT * FROM Win32_DataFile"
WScript.Echo "Waiting for instances."
sink.Cancel()
set sink= Nothing
```



<span data-ttu-id="cfed0-111">Pour plus d’informations sur la construction d’appels de méthode asynchrones dans un script, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cfed0-111">For detailed information about constructing asynchronous method calls in script, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="cfed0-112">Dans les applications C++, une requête asynchrone génère un processus distinct pour recevoir les données de la requête.</span><span class="sxs-lookup"><span data-stu-id="cfed0-112">In C++ applications, an asynchronous query spawns a separate process to receive query data.</span></span> <span data-ttu-id="cfed0-113">Une requête asynchrone est plus complexe qu’une requête synchrone, car vous devez coder une application multithread.</span><span class="sxs-lookup"><span data-stu-id="cfed0-113">An asynchronous query is more complex than a synchronous query, as you must code a multithreaded application.</span></span> <span data-ttu-id="cfed0-114">Toutefois, une requête asynchrone ne monopolise pas le thread principal de votre application.</span><span class="sxs-lookup"><span data-stu-id="cfed0-114">However, an asynchronous query does not monopolize the main thread of your application.</span></span>

<span data-ttu-id="cfed0-115">La procédure suivante décrit comment exécuter une requête asynchrone en C++.</span><span class="sxs-lookup"><span data-stu-id="cfed0-115">The following procedure describes how to perform an asynchronous query in C++.</span></span>

<span data-ttu-id="cfed0-116">**Pour exécuter une requête asynchrone en C++**</span><span class="sxs-lookup"><span data-stu-id="cfed0-116">**To perform an asynchronous query in C++**</span></span>

1.  <span data-ttu-id="cfed0-117">Implémentez un objet **IWbemSink** .</span><span class="sxs-lookup"><span data-stu-id="cfed0-117">Implement an **IWbemSink** object.</span></span>

    <span data-ttu-id="cfed0-118">Un objet **IWbemSink** reçoit des informations sur une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="cfed0-118">An **IWbemSink** object receives information about an asynchronous operation.</span></span>

2.  <span data-ttu-id="cfed0-119">Décrivez votre requête dans un appel à [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span><span class="sxs-lookup"><span data-stu-id="cfed0-119">Describe your query in a call to [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span></span>

    <span data-ttu-id="cfed0-120">WMI déplace immédiatement le processus qui interroge le CIM sur un autre thread et libère le thread qui a exécuté la requête pour une autre tâche.</span><span class="sxs-lookup"><span data-stu-id="cfed0-120">WMI immediately moves the process that queries the CIM to another thread and frees up the thread that executed the query for another task.</span></span>

3.  <span data-ttu-id="cfed0-121">Attendez que WMI appelle la méthode [**IWbemObjectSink :: indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="cfed0-121">Wait for WMI to call the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

    <span data-ttu-id="cfed0-122">Lorsque vous avez terminé, les appels WMI [**indiquent**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) à votre application que la requête est terminée.</span><span class="sxs-lookup"><span data-stu-id="cfed0-122">When finished, WMI calls [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to signal your application that the query is complete.</span></span> <span data-ttu-id="cfed0-123">WMI retourne également les résultats de la requête au récepteur en tant que pointeur vers un pointeur d’interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="cfed0-123">WMI also returns results of the query to the sink as a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="cfed0-124">Comme pour une requête synchrone, utilisez le pointeur pour accéder aux objets qui composent le résultat de votre requête.</span><span class="sxs-lookup"><span data-stu-id="cfed0-124">As with a synchronous query, use the pointer to access the objects that make up the result of your query.</span></span>

<span data-ttu-id="cfed0-125">L’exemple de code suivant ne se compile pas sans erreur, car la classe QuerySink n’a pas été définie.</span><span class="sxs-lookup"><span data-stu-id="cfed0-125">The following code example does not compile without an error because the class QuerySink has not been defined.</span></span> <span data-ttu-id="cfed0-126">Pour obtenir la définition de la classe QuerySink, consultez [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="cfed0-126">For the definition of the QuerySink class, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="cfed0-127">L’exemple de code requiert également les instructions de référence et \# include suivantes.</span><span class="sxs-lookup"><span data-stu-id="cfed0-127">The code example also requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



<span data-ttu-id="cfed0-128">L’exemple de code suivant montre comment effectuer un appel asynchrone pour émettre une requête.</span><span class="sxs-lookup"><span data-stu-id="cfed0-128">The following code example shows how to make an asynchronous call to issue a query.</span></span>


```C++
void ExecQuery(IWbemServices *pSvc)
{
    // Create a new sink object.
    QuerySink *pSink = new QuerySink;

    // Initialize the query and query language.
    BSTR strQuery = SysAllocString(L"SELECT * FROM ClassName");
    BSTR strQueryLang = SysAllocString(L"WQL");
    
    // Issue the query.
    HRESULT hRes = pSvc->ExecQueryAsync(strQueryLang, strQuery, 0,
        NULL, pSink);

    // Clean up.
    SysFreeString(strQuery);
    SysFreeString(strQueryLang);
    
    if (hRes)
    {
        printf("ExecQueryAsync failed with = 0x%X\n", hRes);
        return;
    }
    
    printf("Completed.\n");
}
```



<span data-ttu-id="cfed0-129">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cfed0-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 



