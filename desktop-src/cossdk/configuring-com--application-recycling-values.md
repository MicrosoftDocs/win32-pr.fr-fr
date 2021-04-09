---
description: Vous pouvez utiliser les méthodes suivantes pour configurer les valeurs de recyclage d’applications pour votre application COM+.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Configuration des valeurs de recyclage des applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34c989d81f2e3486adb1d12ec76859a1d28f090
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111443"
---
# <a name="configuring-com-application-recycling-values"></a><span data-ttu-id="a3a7c-103">Configuration des valeurs de recyclage des applications COM+</span><span class="sxs-lookup"><span data-stu-id="a3a7c-103">Configuring COM+ Application Recycling Values</span></span>

<span data-ttu-id="a3a7c-104">Vous pouvez utiliser les méthodes suivantes pour configurer les valeurs de recyclage d’applications pour votre application COM+.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-104">You can use the following methods to configure application recycling values for your COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="a3a7c-105">Vous ne pouvez pas recycler une application COM+ qui a été configurée pour s’exécuter en tant que service Windows.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-105">You cannot recycle a COM+ application that has been configured to run as a Windows service.</span></span> <span data-ttu-id="a3a7c-106">En outre, les applications de bibliothèque disposent des propriétés de recyclage et de regroupement de leur processus hôte.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-106">Also, library applications have the recycling and pooling properties of their host process.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="a3a7c-107">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="a3a7c-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="a3a7c-108">Pour configurer le recyclage d’applications pour une application COM+, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a3a7c-108">To configure application recycling for a COM+ application, use the following steps:</span></span>

1.  <span data-ttu-id="a3a7c-109">Dans l’arborescence de la console de l’outil d’administration Services de composants, cliquez avec le bouton droit sur l’application serveur COM+ que vous souhaitez recycler, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-109">In the console tree of the Component Services administrative tool, right-click the COM+ server application you want to be recycled and then click **Properties**.</span></span>

2.  <span data-ttu-id="a3a7c-110">Dans l’onglet **regroupement & recyclage** , entrez des valeurs pour **limite de durée de vie (minutes)**, **limite de mémoire (Ko)**, **délai d’expiration (minutes)**, **limite d’appel** et **limite d’activation**, en fonction des critères que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-110">On the **Pooling & Recycling** tab, enter values for **Lifetime Limit (minutes)**, **Memory Limit (KB)**, **Expiration Timeout (minutes)**, **Call Limit**, and **Activation Limit**, depending on the criteria you want to use.</span></span>

    -   <span data-ttu-id="a3a7c-111">**Limite de durée de vie** indique le nombre maximal de minutes pendant lesquelles un processus peut s’exécuter avant son recyclage.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-111">**Lifetime Limit** indicates the maximum number of minutes a process can run before it's recycled.</span></span> <span data-ttu-id="a3a7c-112">La plage valide est comprise entre 0 et 30 240 minutes (21 jours).</span><span class="sxs-lookup"><span data-stu-id="a3a7c-112">The valid range is 0 through 30,240 minutes (21 days).</span></span> <span data-ttu-id="a3a7c-113">Le nombre de minutes par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-113">The default number of minutes is 0.</span></span>
    -   <span data-ttu-id="a3a7c-114">La **limite de mémoire** indique la quantité maximale d’utilisation de la mémoire de processus (en kilo-octets) avant le recyclage du processus.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-114">**Memory Limit** indicates the maximum amount of process memory usage (in kilobytes) before recycling the process.</span></span> <span data-ttu-id="a3a7c-115">Si l’utilisation de la mémoire du processus dépasse le nombre spécifié pendant plus d’une minute, le processus est recyclé.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-115">If the process's memory usage exceeds the specified number for longer than one minute, the process is recycled.</span></span> <span data-ttu-id="a3a7c-116">La plage valide est comprise entre 0 et 1 048 576 Ko, et la quantité d’utilisation de la mémoire par défaut est de 0 Ko.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-116">The valid range is 0 through 1,048,576 KB, and the default amount of memory usage is 0 KB.</span></span>
    -   <span data-ttu-id="a3a7c-117">**Délai d’expiration** indique le nombre de minutes à attendre, avant d’être arrêté de force, pour la libération de toutes les références externes aux objets du processus.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-117">**Expiration Timeout** indicates the number of minutes to wait, before being forcibly shut down, for the release of all external references to objects in the process.</span></span> <span data-ttu-id="a3a7c-118">La plage valide est comprise entre 1 et 1440 minutes (24 heures) et le délai d’expiration par défaut est de 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-118">The valid range is 1 through 1440 minutes (24 hours), and the default expiration time-out is 15 minutes.</span></span> <span data-ttu-id="a3a7c-119">Cette valeur est utilisée uniquement lorsqu’il est déjà déterminé qu’un processus sera recyclé selon les autres critères.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-119">This value is used only when it is already determined that a process will be recycled based on the other criteria.</span></span>
    -   <span data-ttu-id="a3a7c-120">**Limite d’appel** indique le nombre maximal d’appels que les objets d’application peuvent accepter avant de recycler le processus.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-120">**Call Limit** indicates the maximum number of calls that application objects can accept before recycling the process.</span></span> <span data-ttu-id="a3a7c-121">La plage valide est comprise entre 0 et 1 048 576 appels, et le nombre d’appels par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-121">The valid range is 0 through 1,048,576 calls, and the default number of calls is 0.</span></span>
    -   <span data-ttu-id="a3a7c-122">**Limite d’activation** indique le nombre maximal d’activations d’objets d’application à accepter avant de recycler le processus.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-122">**Activation Limit** indicates the maximum number of application object activations to accept before recycling the process.</span></span> <span data-ttu-id="a3a7c-123">La plage valide est comprise entre 0 et 1 048 576 activations, et le nombre d’activations par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-123">The valid range is 0 through 1,048,576 activations, and the default number of activations is 0.</span></span>

    > [!Note]  
    > <span data-ttu-id="a3a7c-124">Lorsque la limite de **durée de vie**, la limite de **mémoire**, la **limite d’appel** ou la valeur de limite d' **activation** est définie sur 0 (valeur par défaut), le recyclage d’applications pour ce critère est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-124">When the **Lifetime Limit**, **Memory Limit**, **Call Limit**, or **Activation Limit** value is set to 0 (the default value), application recycling for that criterion is disabled.</span></span> <span data-ttu-id="a3a7c-125">Lorsque les quatre critères ont la valeur 0, le recyclage de l’application est désactivé pour l’application sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-125">When all four of these criteria are set to 0, application recycling is disabled for the selected application.</span></span>

     

3.  <span data-ttu-id="a3a7c-126">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-126">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="a3a7c-127">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a3a7c-127">Visual Basic</span></span>

<span data-ttu-id="a3a7c-128">La fonction suivante dans Microsoft Visual Basic montre comment vous pouvez définir les valeurs de recyclage d’application pour n’importe quelle application serveur COM+ que vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-128">The following function in Microsoft Visual Basic demonstrates how you can set the application recycling values for any COM+ server application that you choose.</span></span> <span data-ttu-id="a3a7c-129">Pour l’utiliser à partir de Visual Basic, ajoutez une référence à la bibliothèque de types d’administration COM+.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-129">To use it from Visual Basic, add a reference to the COM+ Admin Type Library.</span></span>


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



<span data-ttu-id="a3a7c-130">Pour utiliser la fonction, fournissez une valeur de chaîne pour le nom de l’application et les valeurs entières pour les paramètres de recyclage d’application souhaités.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-130">To use the function, provide a string value for the application name and integer values for the desired application recycling settings.</span></span> <span data-ttu-id="a3a7c-131">Le code Visual Basic suivant montre comment définir la valeur **RecycleLifetimeLimit** sur 5, la valeur **RecycleMemoryLimit** sur 10, la valeur **RecycleCallLimit** sur 9, la valeur **RecycleActivationLimit** sur 100 et la valeur **RecycleExpirationTimeout** sur 15.</span><span class="sxs-lookup"><span data-stu-id="a3a7c-131">The following Visual Basic code shows how to set the **RecycleLifetimeLimit** value to 5, the **RecycleMemoryLimit** value to 10, the **RecycleCallLimit** value to 9, the **RecycleActivationLimit** value to 100, and the **RecycleExpirationTimeout** value to 15.</span></span>


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a><span data-ttu-id="a3a7c-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3a7c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3a7c-133">Concepts de recyclage des applications COM+</span><span class="sxs-lookup"><span data-stu-id="a3a7c-133">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



