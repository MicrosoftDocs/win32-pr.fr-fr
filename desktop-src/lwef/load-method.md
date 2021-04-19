---
title: Load, méthode
description: Load, méthode
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927fc8e49e55c2bdfcd7b1109bb8604540c199c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509651"
---
# <a name="load-method"></a><span data-ttu-id="79978-103">Load, méthode</span><span class="sxs-lookup"><span data-stu-id="79978-103">Load Method</span></span>

<span data-ttu-id="79978-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="79978-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="79978-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="79978-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="79978-106">Charge un caractère dans la collection de [**caractères**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="79978-106">Loads a character into the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="79978-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="79978-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="79978-108">\*agent ***. Caractères. Load "*** CharacterID \* \* *",* \*  *fournisseur*</span><span class="sxs-lookup"><span data-stu-id="79978-108">*agent ***.Characters.Load "*** CharacterID\*\*\*",*\* *Provider*</span></span>



| <span data-ttu-id="79978-109">Partie</span><span class="sxs-lookup"><span data-stu-id="79978-109">Part</span></span>          | <span data-ttu-id="79978-110">Description</span><span class="sxs-lookup"><span data-stu-id="79978-110">Description</span></span>                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79978-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="79978-111">*CharacterID*</span></span> | <span data-ttu-id="79978-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="79978-112">Required.</span></span> <span data-ttu-id="79978-113">Valeur de chaîne que vous allez utiliser pour faire référence aux données caractères à charger.</span><span class="sxs-lookup"><span data-stu-id="79978-113">A string value that you will use to refer to the character data to be loaded.</span></span>                                                                                                                                                  |
| <span data-ttu-id="79978-114">*Fournisseur*</span><span class="sxs-lookup"><span data-stu-id="79978-114">*Provider*</span></span>    | <span data-ttu-id="79978-115">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="79978-115">Required.</span></span> <span data-ttu-id="79978-116">Type de données Variant qui doit être l’un des éléments suivants : **spécification** de l’emplacement du fichier local du fichier de définition du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="79978-116">A variant data type that must be one of the following: **Filespec** The local file location of the specified character's definition file.</span></span> <br/> <span data-ttu-id="79978-117">**URL** Adresse HTTP du fichier de définition du caractère.</span><span class="sxs-lookup"><span data-stu-id="79978-117">**URL** The HTTP address for the character's definition file.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79978-118">Notes</span><span class="sxs-lookup"><span data-stu-id="79978-118">Remarks</span></span>

<span data-ttu-id="79978-119">Vous pouvez charger des caractères à partir du sous-répertoire de l’agent en spécifiant un chemin d’accès relatif (qui n’inclut pas de signe deux-points ou de barre oblique de début).</span><span class="sxs-lookup"><span data-stu-id="79978-119">You can load characters from the Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="79978-120">Cela préfixe le chemin d’accès avec le répertoire de caractères de l’agent (situé dans le \\ répertoire msagent Windows localisé).</span><span class="sxs-lookup"><span data-stu-id="79978-120">This prefixes the path with Agent's characters directory (located in the localized Windows\\msagent directory).</span></span> <span data-ttu-id="79978-121">Par exemple, si vous spécifiez ce qui suit, génie. ACS est chargé à partir du répertoire de caractères de l’agent :</span><span class="sxs-lookup"><span data-stu-id="79978-121">For example, specifying the following would load Genie.acs from Agent's Chars directory:</span></span>


```
   Agent.Character.Load "genie", "genie.acs"
```



<span data-ttu-id="79978-122">Vous pouvez également spécifier votre propre répertoire dans le répertoire de caractères de l’agent.</span><span class="sxs-lookup"><span data-stu-id="79978-122">You can also specify your own directory in Agent's Chars directory.</span></span>


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



<span data-ttu-id="79978-123">Vous pouvez charger le caractère actuellement défini en tant que caractère par défaut de l’utilisateur actuel en n’incluant pas de chemin d’accès comme deuxième paramètre de la méthode **Load** .</span><span class="sxs-lookup"><span data-stu-id="79978-123">You can load the character currently set as the current user's default character by not including a path as the second parameter of the **Load** method.</span></span>


```
   Agent.Character.Load "character"
```



<span data-ttu-id="79978-124">Vous ne pouvez pas charger le même caractère (un caractère ayant le même GUID) plusieurs fois à partir d’une seule instance du contrôle.</span><span class="sxs-lookup"><span data-stu-id="79978-124">You cannot load the same character (a character having the same GUID) more than once from a single instance of the control.</span></span> <span data-ttu-id="79978-125">De même, vous ne pouvez pas charger le caractère par défaut et d’autres caractères en même temps à partir d’une seule instance du contrôle, car le caractère par défaut peut être identique à l’autre caractère.</span><span class="sxs-lookup"><span data-stu-id="79978-125">Similarly, you cannot load the default character and other characters at the same time from a single instance of the control because the default character could be the same as the other character.</span></span> <span data-ttu-id="79978-126">Si vous tentez de le faire, le serveur génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="79978-126">If you attempt to do this, the server raises an error.</span></span> <span data-ttu-id="79978-127">Toutefois, vous pouvez créer une autre instance du contrôle de l’agent et charger le même caractère.</span><span class="sxs-lookup"><span data-stu-id="79978-127">However, you can create another instance of the Agent control and load the same character.</span></span>

<span data-ttu-id="79978-128">Microsoft Agent Fournisseur de données prend en charge le chargement de données de type caractère stockées dans un fichier structuré unique (. ACS) avec des données de caractères et des données d’animation, ainsi que des données de caractères distinctes (. ACF) et d’animation (. ).</span><span class="sxs-lookup"><span data-stu-id="79978-128">The Microsoft Agent Data Provider supports loading character data stored either as a single structured file (.ACS) with character data and animation data together or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="79978-129">Utilisez l’unique structure structurée. Fichier ACS pour charger un caractère stocké sur un disque local ou un réseau et accessible à l’aide d’un protocole de fichiers conventionnel (tel que les chemins d’accès UNC).</span><span class="sxs-lookup"><span data-stu-id="79978-129">Use the single structured .ACS file to load a character that is stored on a local disk or network and accessed using a conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="79978-130">Utilisez le distinct. ACF et. Les fichiers de CCN lorsque vous souhaitez charger les fichiers d’animation individuellement à partir d’un site distant où ils sont accessibles à l’aide du protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="79978-130">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using the HTTP protocol.</span></span>

<span data-ttu-id="79978-131">Pour. Les fichiers ACS, à l’aide de la méthode **Load** , permettent d’accéder aux animations d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="79978-131">For .ACS files, using the **Load** method provides access to a character's animations.</span></span> <span data-ttu-id="79978-132">Pour. Fichiers ACF, vous utilisez également la méthode d' [**extraction**](get-method.md) pour charger des données d’animation.</span><span class="sxs-lookup"><span data-stu-id="79978-132">For .ACF files, you also use the [**Get**](get-method.md) method to load animation data.</span></span> <span data-ttu-id="79978-133">La méthode **Load** ne prend pas en charge le téléchargement. Fichiers ACS à partir d’un site HTTP.</span><span class="sxs-lookup"><span data-stu-id="79978-133">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="79978-134">Le chargement d’un caractère n’affiche pas automatiquement le caractère.</span><span class="sxs-lookup"><span data-stu-id="79978-134">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="79978-135">Utilisez d’abord la méthode [**Show**](show-method.md) pour rendre le caractère visible.</span><span class="sxs-lookup"><span data-stu-id="79978-135">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

<span data-ttu-id="79978-136">Si vous utilisez la méthode **Load** pour charger un fichier de caractères stocké sur l’ordinateur local et que l’appel échoue ; par exemple, étant donné que le fichier est introuvable, l’agent génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="79978-136">If you use the **Load** method to load a character file stored on the local machine and the call fails; for example, because the file is not found, Agent raises an error.</span></span> <span data-ttu-id="79978-137">Vous pouvez utiliser la prise en charge dans votre langage de programmation pour fournir une routine de gestion des erreurs pour intercepter et traiter l’erreur.</span><span class="sxs-lookup"><span data-stu-id="79978-137">You can use the support in your programming language to provide an error handling routine to catch and process the error.</span></span>


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



<span data-ttu-id="79978-138">Vous pouvez également gérer l’erreur en affectant à [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) la **valeur false**, en déclarant un objet et en lui assignant la demande de **chargement** .</span><span class="sxs-lookup"><span data-stu-id="79978-138">You can also handle the error by setting [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) to **False**, declaring a object, and assigning the **Load** request to it.</span></span> <span data-ttu-id="79978-139">Suivez ensuite l’appel de **chargement** avec une instruction qui vérifie l’état de l’objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="79978-139">Then follow the **Load** call with a statement that checks the status of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



<span data-ttu-id="79978-140">Si vous chargez un caractère qui n’est pas local ; par exemple, à l’aide du protocole HTTP, vous pouvez également rechercher un échec de **chargement** en affectant un objet de [**requête**](/windows/desktop/lwef/the-request-object) à la méthode **Load** .</span><span class="sxs-lookup"><span data-stu-id="79978-140">If you load a character that is not local; for example, using HTTP protocol, you can also check for a **Load** failure by assigning a [**Request**](/windows/desktop/lwef/the-request-object) object to the **Load** method.</span></span> <span data-ttu-id="79978-141">Toutefois, étant donné que cette méthode de chargement d’un caractère est gérée de façon asynchrone, vérifiez son état dans l’événement [**RequestComplete**](requestcomplete-event.md) .</span><span class="sxs-lookup"><span data-stu-id="79978-141">However, because this method of loading a character is handled asynchronously, check its status in the [**RequestComplete**](requestcomplete-event.md) event.</span></span> <span data-ttu-id="79978-142">Cette technique ne fonctionne pas en chargeant un caractère à l’aide du protocole UNC, car la méthode **Load** est traitée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="79978-142">This technique will not work loading a character using the UNC protocol because the **Load** method is processed synchronously.</span></span>

 

