---
title: Propriété Connected
description: Propriété Connected
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bba78358c7c42f0754da017aa0c188d41acd189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310585"
---
# <a name="connected-property"></a><span data-ttu-id="f616b-103">Propriété Connected</span><span class="sxs-lookup"><span data-stu-id="f616b-103">Connected Property</span></span>

<span data-ttu-id="f616b-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f616b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f616b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="f616b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f616b-106">Retourne ou définit une valeur indiquant si le contrôle en cours est connecté au serveur Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f616b-106">Returns or sets whether the current control is connected to the Microsoft Agent server.</span></span>

</dd> <dt>

<span data-ttu-id="f616b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="f616b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f616b-108">*agent. \* \* \* connecté* \*  \[  =  *valeur booléenne*\]</span><span class="sxs-lookup"><span data-stu-id="f616b-108">*agent.\*\*\*Connected*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="f616b-109">Partie</span><span class="sxs-lookup"><span data-stu-id="f616b-109">Part</span></span>      | <span data-ttu-id="f616b-110">Description</span><span class="sxs-lookup"><span data-stu-id="f616b-110">Description</span></span>                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f616b-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="f616b-111">*boolean*</span></span> | <span data-ttu-id="f616b-112">Expression booléenne spécifiant si le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="f616b-112">A Boolean expression specifying whether the control is connected.</span></span> <span data-ttu-id="f616b-113">**True** Le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="f616b-113">**True** The control is connected.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f616b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f616b-114">Remarks</span></span>

<span data-ttu-id="f616b-115">Dans de nombreux cas, la spécification du contrôle crée automatiquement une connexion avec le serveur Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f616b-115">In many situations, specifying the control automatically creates a connection with the Microsoft Agent server.</span></span> <span data-ttu-id="f616b-116">Par exemple, la spécification du CLSID du contrôle Microsoft Agent dans la <OBJECT> balise d’une page Web ouvre automatiquement une connexion au serveur et la fermeture de la page ferme la connexion.</span><span class="sxs-lookup"><span data-stu-id="f616b-116">For example, specifying the Microsoft Agent control's CLSID in the <OBJECT> tag in a webpage automatically opens a server connection and exiting the page closes the connection.</span></span> <span data-ttu-id="f616b-117">De même, pour les Visual Basic ou d’autres langages qui vous permettent de supprimer un contrôle dans un formulaire, l’exécution automatique du programme ouvre une connexion et la fermeture du programme ferme la connexion.</span><span class="sxs-lookup"><span data-stu-id="f616b-117">Similarly, for Visual Basic or other languages that enable you to drop a control on a form, running the program automatically opens a connection and exiting the program closes the connection.</span></span> <span data-ttu-id="f616b-118">Si le serveur n’est pas en cours d’exécution, il démarre automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f616b-118">If the server isn't currently running, it automatically starts.</span></span>

<span data-ttu-id="f616b-119">Toutefois, si vous souhaitez créer un contrôle d’agent au moment de l’exécution, vous devrez peut-être également ouvrir explicitement une nouvelle connexion au serveur à l’aide de la propriété **Connected** .</span><span class="sxs-lookup"><span data-stu-id="f616b-119">However, if you want to create an Agent control at run time, you may also need to explicitly open a new connection to the server using the **Connected** property.</span></span> <span data-ttu-id="f616b-120">Par exemple, dans Visual Basic vous pouvez créer un objet ActiveX au moment de l’exécution à l’aide de l’instruction Set avec le mot clé **New** (ou la fonction CreateObject).</span><span class="sxs-lookup"><span data-stu-id="f616b-120">For example, in Visual Basic you can create an ActiveX object at run time using the Set statement with the **New** keyword (or CreateObject function).</span></span> <span data-ttu-id="f616b-121">Bien que cette opération crée l’objet, elle risque de ne pas créer la connexion au serveur.</span><span class="sxs-lookup"><span data-stu-id="f616b-121">While this creates the object, it may not create the connection to the server.</span></span> <span data-ttu-id="f616b-122">Vous pouvez utiliser la propriété **Connected** avant tout code qui appelle l’interface de programmation de Microsoft Agent, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="f616b-122">You can use the **Connected** property before any code that calls into Microsoft Agent's programming interface, as shown in the following example:</span></span>


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



<span data-ttu-id="f616b-123">La création d’un contrôle à l’aide de cette technique n’expose pas les événements du contrôle de l’agent.</span><span class="sxs-lookup"><span data-stu-id="f616b-123">Creating a control using this technique does not expose the Agent control's events.</span></span> <span data-ttu-id="f616b-124">Dans Visual Basic 5,0 (et versions ultérieures), vous pouvez accéder aux événements du contrôle en incluant le contrôle dans les références de votre projet, et utiliser le mot clé **WithEvents** dans votre déclaration de variable :</span><span class="sxs-lookup"><span data-stu-id="f616b-124">In Visual Basic 5.0 (and later), you can access the control's events by including the control in your project's references, and use the **WithEvents** keyword in your variable declaration:</span></span>


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



<span data-ttu-id="f616b-125">L’utilisation de **WithEvents** pour créer une instance du contrôle de l’agent au moment de l’exécution ouvre automatiquement la connexion avec le serveur Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f616b-125">Using **WithEvents** to create an instance of the Agent control at run time automatically opens the connection with the Microsoft Agent server.</span></span> <span data-ttu-id="f616b-126">Par conséquent, vous n’avez pas besoin d’inclure une instruction **connectée** .</span><span class="sxs-lookup"><span data-stu-id="f616b-126">Therefore, you don't need to include a **Connected** statement.</span></span>

<span data-ttu-id="f616b-127">Vous pouvez fermer votre connexion au serveur en libérant toutes les références que vous avez créées aux objets de l’agent, par exemple IAgentCtlCharacterEx et IAgentCtlCommandEx.</span><span class="sxs-lookup"><span data-stu-id="f616b-127">You can close your connection to the server by releasing all references you created to Agent objects, such as IAgentCtlCharacterEx and IAgentCtlCommandEx.</span></span> <span data-ttu-id="f616b-128">Vous devez également libérer votre référence au contrôle de l’agent lui-même.</span><span class="sxs-lookup"><span data-stu-id="f616b-128">You must also release your reference to the Agent control itself.</span></span> <span data-ttu-id="f616b-129">Dans Visual Basic, vous pouvez publier une référence à un objet en affectant à sa variable la valeur **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="f616b-129">In Visual Basic, you can release a reference to an object by setting its variable to **Nothing**.</span></span> <span data-ttu-id="f616b-130">Si vous avez chargé des caractères, déchargez-les avant de libérer l’objet caractère.</span><span class="sxs-lookup"><span data-stu-id="f616b-130">If you have loaded characters, unload them before releasing the character object.</span></span>


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> <span data-ttu-id="f616b-131">Vous ne pouvez pas fermer votre connexion au serveur en libérant les références où le composant a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="f616b-131">You cannot close your connection to the server by releasing references where the component has been added.</span></span> <span data-ttu-id="f616b-132">Par exemple, vous ne pouvez pas fermer votre connexion au serveur sur des pages Web où vous utilisez la <OBJECT> balise pour déclarer le contrôle ou dans une application de Visual Basic où vous déposez le contrôle sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="f616b-132">For example, you cannot close your connection to the server on webpages where you use the <OBJECT> tag to declare the control or in a Visual Basic application where you drop the control on a form.</span></span> <span data-ttu-id="f616b-133">Si la libération de toutes les références d’agent réduit la plage de travail de l’agent, la connexion est conservée jusqu’à ce que vous atteigniez la page suivante ou que vous quittiez l’application.</span><span class="sxs-lookup"><span data-stu-id="f616b-133">While releasing all Agent references will reduce Agent's working set, the connection remains until you navigate to the next page or exit the application.</span></span>

 

 

 





