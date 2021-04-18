---
title: Informations de registre des contrôles ActiveX
description: Informations de registre des contrôles ActiveX
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508149"
---
# <a name="activex-controls-registry-information"></a><span data-ttu-id="92257-103">Informations de registre des contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="92257-103">ActiveX Controls Registry Information</span></span>

<span data-ttu-id="92257-104">Un certain nombre d’entrées de Registre et d’indicateurs sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="92257-104">There are a number of registry entries and flags that are used.</span></span> <span data-ttu-id="92257-105">En outre, les contrôles peuvent prendre en charge des catégories de composants pour classer les fonctionnalités qu’ils fournissent.</span><span class="sxs-lookup"><span data-stu-id="92257-105">Additionally, controls can support component categories to classify the features they provide.</span></span>

<span data-ttu-id="92257-106">Les clés de Registre liées aux contrôles sont signalées par un astérisque dans l’arborescence suivante :</span><span class="sxs-lookup"><span data-stu-id="92257-106">Registry keys related to controls are marked with an asterisk in the following tree:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

<span data-ttu-id="92257-107">L’entrée **DefaultIcon** est utilisée pour identifier une icône à afficher lorsque le contrôle est réduit à une icône.</span><span class="sxs-lookup"><span data-stu-id="92257-107">The **DefaultIcon** entry is used to identify an icon to be displayed when the control is minimized to an icon.</span></span> <span data-ttu-id="92257-108">La fonction [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) est utilisée pour récupérer l’icône à partir de. DLL ou. Fichier exécutable spécifié.</span><span class="sxs-lookup"><span data-stu-id="92257-108">The [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) function is used to get the icon from the .DLL or .EXE file specified.</span></span>

<span data-ttu-id="92257-109">L’entrée **ToolboxBitmap32** identifie le nom du module et l’identificateur de ressource pour une \* image bitmap 16 15 à utiliser pour la face d’un bouton de barre d’outils ou de boîte à outils.</span><span class="sxs-lookup"><span data-stu-id="92257-109">The **ToolboxBitmap32** entry identifies the module name and resource identifier for a 16\*15 bitmap to use for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="92257-110">La taille de l’icône Windows standard est trop grande pour être utilisée à cet effet.</span><span class="sxs-lookup"><span data-stu-id="92257-110">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="92257-111">Cette entrée prend en charge spécifiquement les conteneurs de contrôle qui ont un mode création dans lequel l’un sélectionne les contrôles et les place sur un formulaire en cours de conception.</span><span class="sxs-lookup"><span data-stu-id="92257-111">This entry specifically supports control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span> <span data-ttu-id="92257-112">Par exemple, dans Visual Basic, l’icône du contrôle s’affiche dans la boîte à outils Visual Basic en mode Design.</span><span class="sxs-lookup"><span data-stu-id="92257-112">For example, in Visual Basic, the control's icon is displayed in the Visual Basic toolbox during design mode.</span></span>

<span data-ttu-id="92257-113">L’entrée de **contrôle** marque un objet en tant que contrôle.</span><span class="sxs-lookup"><span data-stu-id="92257-113">The **Control** entry marks an object as a control.</span></span> <span data-ttu-id="92257-114">Cette entrée est souvent utilisée par les conteneurs pour remplir des boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="92257-114">This entry is often used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="92257-115">Le conteneur utilise cette sous-clé pour déterminer s’il faut inclure un objet dans une boîte de dialogue qui affiche des contrôles.</span><span class="sxs-lookup"><span data-stu-id="92257-115">The container uses this sub-key to determine whether to include an object in a dialog box that displays controls.</span></span>

<span data-ttu-id="92257-116">La sous-clé pouvant être **insérée** peut également être utilisée avec des contrôles, selon que l’objet peut agir uniquement comme un objet incorporé sur place sans fonctionnalités de contrôle spéciales.</span><span class="sxs-lookup"><span data-stu-id="92257-116">The **Insertable** sub-key can also be used with controls, depending on whether the object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="92257-117">Les objets marqués avec l’option d' **insertion** s’affichent dans la boîte de dialogue Insérer un objet de leur conteneur.</span><span class="sxs-lookup"><span data-stu-id="92257-117">Objects marked with **Insertable** appear in the Insert Object dialog box of their container.</span></span> <span data-ttu-id="92257-118">L’entrée pouvant être **insérée** signifie généralement que le contrôle a été testé avec des conteneurs sans contrôle.</span><span class="sxs-lookup"><span data-stu-id="92257-118">The **Insertable** entry generally means that the control has been tested with non-control containers.</span></span>

<span data-ttu-id="92257-119">Les sous-clés d' **insertion** et de **contrôle** sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="92257-119">Both the **Insertable** and the **Control** sub-keys are optional.</span></span> <span data-ttu-id="92257-120">Un contrôle peut omettre la sous-clé pouvant être **insérée** s’il n’est pas conçu pour fonctionner avec des conteneurs plus anciens qui ne comprennent pas de contrôles.</span><span class="sxs-lookup"><span data-stu-id="92257-120">A control can omit the **Insertable** sub-key if it not designed to work with older containers that do not understand controls.</span></span> <span data-ttu-id="92257-121">Un contrôle peut omettre la touche de **contrôle** s’il est conçu uniquement pour fonctionner avec un conteneur spécifique et ne souhaite donc pas être inséré dans d’autres conteneurs.</span><span class="sxs-lookup"><span data-stu-id="92257-121">A control can omit the **Control** key if it is only designed to work with a specific container and thus does not wish to be inserted in other containers.</span></span>

<span data-ttu-id="92257-122">Les contrôles doivent avoir un verbe Properties, OLEIVERB \_ Properties, ainsi que tous les autres verbes qu’ils prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="92257-122">Controls should have a Properties verb, OLEIVERB\_PROPERTIES, along with any other verbs they support.</span></span> <span data-ttu-id="92257-123">Le verbe Properties, ainsi que le verbe standard OLEIVERB \_ Primary, fait en sorte que le contrôle affiche sa feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="92257-123">The Properties verb, as well as the standard verb OLEIVERB\_PRIMARY, instructs the control to display its property sheet.</span></span> <span data-ttu-id="92257-124">Le verbe Properties est affiché en tant qu’élément Properties dans le menu du conteneur lorsque le contrôle est actif.</span><span class="sxs-lookup"><span data-stu-id="92257-124">The Properties verb is displayed as the Properties item on the container's menu when the control is active.</span></span> <span data-ttu-id="92257-125">De cette façon, le contrôle peut afficher sa propre page de propriétés, ce qui permet à l’utilisateur final de disposer de fonctionnalités utiles, même si le conteneur ne gère pas les contrôles.</span><span class="sxs-lookup"><span data-stu-id="92257-125">This way, the control can display its own property page allowing some useful functionality to the end user, even if the container does not handle controls.</span></span>

<span data-ttu-id="92257-126">Un contrôle définit la clé **MiscStatus** pour se décrire aux conteneurs potentiels.</span><span class="sxs-lookup"><span data-stu-id="92257-126">A control defines the **MiscStatus** key to describe itself to potential containers.</span></span> <span data-ttu-id="92257-127">Les bits prennent les valeurs de [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc), et les contrôles ajoutent plusieurs valeurs à cette énumération.</span><span class="sxs-lookup"><span data-stu-id="92257-127">The bits take on the values from [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc), and controls add several values to this enumeration.</span></span> <span data-ttu-id="92257-128">Pour plus d’informations, consultez les valeurs d’énumération **OLEMISC** .</span><span class="sxs-lookup"><span data-stu-id="92257-128">See the **OLEMISC** enumeration values for more information.</span></span> <span data-ttu-id="92257-129">Le client peut obtenir ces informations en appelant [**IOleObject :: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) sans avoir à instancier le contrôle en premier.</span><span class="sxs-lookup"><span data-stu-id="92257-129">The client can obtain this information by calling [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) without having to instantiate the control first.</span></span>

<span data-ttu-id="92257-130">Enfin, **version** décrit la version du contrôle qui doit correspondre à la version de la bibliothèque de types associée à ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="92257-130">Finally, **Version** describes the version of the control which should match the version of the type library associated with this control.</span></span>

<span data-ttu-id="92257-131">De même, dans les informations de type pour un contrôle, le contrôle d’attribut marque une entrée de coclasse comme décrivant un contrôle.</span><span class="sxs-lookup"><span data-stu-id="92257-131">Also in the type information for a control, the attribute control marks a coclass entry as describing a control.</span></span>

 

 