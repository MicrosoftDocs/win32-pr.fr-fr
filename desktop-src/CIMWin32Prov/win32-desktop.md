---
description: La \_ classe DesktopWMI Win32 représente les caractéristiques courantes du Bureau d’un utilisateur. Les propriétés de cette classe peuvent être modifiées par l’utilisateur pour personnaliser le bureau.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Classe Win32_Desktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d005104cb663a680bac080b7ff9b6529fd9b7a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861718"
---
# <a name="win32_desktop-class"></a><span data-ttu-id="91d82-104">\_Classe de bureau Win32</span><span class="sxs-lookup"><span data-stu-id="91d82-104">Win32\_Desktop class</span></span>

<span data-ttu-id="91d82-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) du **\_ Bureau Win32** représente les caractéristiques courantes du Bureau d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="91d82-105">The **Win32\_Desktop**[WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the common characteristics of a user's desktop.</span></span> <span data-ttu-id="91d82-106">Les propriétés de cette classe peuvent être modifiées par l’utilisateur pour personnaliser le bureau.</span><span class="sxs-lookup"><span data-stu-id="91d82-106">The properties of this class can be modified by the user to customize the desktop.</span></span>

<span data-ttu-id="91d82-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="91d82-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="91d82-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="91d82-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d82-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91d82-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a><span data-ttu-id="91d82-110">Membres</span><span class="sxs-lookup"><span data-stu-id="91d82-110">Members</span></span>

<span data-ttu-id="91d82-111">La **classe \_ Desktop Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="91d82-111">The **Win32\_Desktop** class has these types of members:</span></span>

-   [<span data-ttu-id="91d82-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91d82-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91d82-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91d82-113">Properties</span></span>

<span data-ttu-id="91d82-114">La **classe \_ Bureau Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="91d82-114">The **Win32\_Desktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91d82-115">**BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="91d82-115">**BorderWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-116">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91d82-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-118">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Bureau \\ \\ WindowMetrics \| BorderWidth»)</span><span class="sxs-lookup"><span data-stu-id="91d82-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|BorderWidth")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-119">Largeur des bordures autour de toutes les fenêtres avec des bordures réglables.</span><span class="sxs-lookup"><span data-stu-id="91d82-119">Width of the borders around all windows with adjustable borders.</span></span>

<span data-ttu-id="91d82-120">Exemple : 3</span><span class="sxs-lookup"><span data-stu-id="91d82-120">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="91d82-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="91d82-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d82-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-124">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="91d82-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="91d82-125">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="91d82-125">Short textual description of the current object.</span></span>

<span data-ttu-id="91d82-126">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="91d82-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d82-127">**CoolSwitch**</span><span class="sxs-lookup"><span data-stu-id="91d82-127">**CoolSwitch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="91d82-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-130">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| panneau de configuration \\ \\ Desktop \| CoolSwitch »)</span><span class="sxs-lookup"><span data-stu-id="91d82-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CoolSwitch")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-131">Le changement rapide de tâches est activé.</span><span class="sxs-lookup"><span data-stu-id="91d82-131">Fast task switching is turned on.</span></span> <span data-ttu-id="91d82-132">Le changement rapide de tâches permet à l’utilisateur de basculer entre les fenêtres à l’aide de la combinaison de touches **Alt + Tab** .</span><span class="sxs-lookup"><span data-stu-id="91d82-132">Fast task switching allows the user to switch between windows using the **ALT+TAB** keyboard combination.</span></span>

</dd> <dt>

<span data-ttu-id="91d82-133">**CursorBlinkRate**</span><span class="sxs-lookup"><span data-stu-id="91d82-133">**CursorBlinkRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91d82-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-136">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| panneau de configuration \\ \\ \| CursorBlinkRate"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondes")</span><span class="sxs-lookup"><span data-stu-id="91d82-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CursorBlinkRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-137">Durée entre les clignotements successifs du curseur.</span><span class="sxs-lookup"><span data-stu-id="91d82-137">Length of time between successive cursor blinks.</span></span>

<span data-ttu-id="91d82-138">Exemple : 530</span><span class="sxs-lookup"><span data-stu-id="91d82-138">Example: 530</span></span>

</dd> <dt>

<span data-ttu-id="91d82-139">**Description**</span><span class="sxs-lookup"><span data-stu-id="91d82-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d82-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91d82-142">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="91d82-142">Textual description of the current object.</span></span>

<span data-ttu-id="91d82-143">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="91d82-143">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d82-144">**DragFullWindows**</span><span class="sxs-lookup"><span data-stu-id="91d82-144">**DragFullWindows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-145">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="91d82-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-147">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| panneau de configuration \\ \\ Desktop \| DragFullWindows »)</span><span class="sxs-lookup"><span data-stu-id="91d82-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|DragFullWindows")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-148">Le contenu d’une fenêtre s’affiche lorsqu’un utilisateur déplace la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="91d82-148">Contents of a window are shown when a user moves the window.</span></span>

</dd> <dt>

<span data-ttu-id="91d82-149">**GridGranularity**</span><span class="sxs-lookup"><span data-stu-id="91d82-149">**GridGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-150">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91d82-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-152">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| panneau de configuration \\ \\ \| GridGranularity"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixels")</span><span class="sxs-lookup"><span data-stu-id="91d82-152">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|GridGranularity"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixels")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-153">Espacement de la grille à laquelle les fenêtres sont liées sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="91d82-153">Spacing of the grid that windows are bound to on the desktop.</span></span> <span data-ttu-id="91d82-154">Cela facilite l’Organisation des fenêtres.</span><span class="sxs-lookup"><span data-stu-id="91d82-154">This makes organizing windows easier.</span></span> <span data-ttu-id="91d82-155">L’espacement est généralement suffisamment précis pour que l’utilisateur ne le remarque pas.</span><span class="sxs-lookup"><span data-stu-id="91d82-155">The spacing is usually fine enough that the user does not notice it.</span></span>

<span data-ttu-id="91d82-156">Exemple : 1</span><span class="sxs-lookup"><span data-stu-id="91d82-156">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="91d82-157">**IconSpacing**</span><span class="sxs-lookup"><span data-stu-id="91d82-157">**IconSpacing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-158">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91d82-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-160">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \\ \\ WindowMetrics \| IconSpacing "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="91d82-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconSpacing"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-161">Espacement entre les icônes.</span><span class="sxs-lookup"><span data-stu-id="91d82-161">Spacing between icons.</span></span>

<span data-ttu-id="91d82-162">Exemple : 75</span><span class="sxs-lookup"><span data-stu-id="91d82-162">Example: 75</span></span>

</dd> <dt>

<span data-ttu-id="91d82-163">**IconTitleFaceName**</span><span class="sxs-lookup"><span data-stu-id="91d82-163">**IconTitleFaceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d82-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-166">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \\ \\ WindowMetrics \| IconFont»)</span><span class="sxs-lookup"><span data-stu-id="91d82-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconFont")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-167">Police utilisée pour les noms des icônes.</span><span class="sxs-lookup"><span data-stu-id="91d82-167">Font used for the names of the icons.</span></span>

<span data-ttu-id="91d82-168">Exemple : « MS San Serif »</span><span class="sxs-lookup"><span data-stu-id="91d82-168">Example: "MS San Serif"</span></span>

</dd> <dt>

<span data-ttu-id="91d82-169">**IconTitleSize**</span><span class="sxs-lookup"><span data-stu-id="91d82-169">**IconTitleSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-170">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91d82-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-172">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| font and Text structures \| [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")</span><span class="sxs-lookup"><span data-stu-id="91d82-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Font and Text Structures\|[**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta)\|lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-173">Taille de police de l’icône.</span><span class="sxs-lookup"><span data-stu-id="91d82-173">Icon font size.</span></span>

<span data-ttu-id="91d82-174">Exemple : 9</span><span class="sxs-lookup"><span data-stu-id="91d82-174">Example: 9</span></span>

</dd> <dt>

<span data-ttu-id="91d82-175">**IconTitleWrap**</span><span class="sxs-lookup"><span data-stu-id="91d82-175">**IconTitleWrap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-176">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="91d82-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-178">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \\ \\ WindowMetrics \| IconTitleWrap»)</span><span class="sxs-lookup"><span data-stu-id="91d82-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconTitleWrap")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-179">Le texte du titre de l’icône revient à la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="91d82-179">Icon's title text wraps to the next line.</span></span>

</dd> <dt>

<span data-ttu-id="91d82-180">**Nom**</span><span class="sxs-lookup"><span data-stu-id="91d82-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d82-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-183">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="91d82-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-184">Nom qui identifie le profil de bureau actuel.</span><span class="sxs-lookup"><span data-stu-id="91d82-184">Name that identifies the current desktop profile.</span></span>

<span data-ttu-id="91d82-185">Exemple : « MainProf »</span><span class="sxs-lookup"><span data-stu-id="91d82-185">Example: "MainProf"</span></span>

</dd> <dt>

<span data-ttu-id="91d82-186">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="91d82-186">**Pattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d82-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-189">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Modèle de bureau du panneau de configuration par défaut \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="91d82-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Pattern")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-190">Nom du modèle utilisé comme arrière-plan du bureau.</span><span class="sxs-lookup"><span data-stu-id="91d82-190">Name of the pattern used as the background for the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="91d82-191">**ScreenSaverActive**</span><span class="sxs-lookup"><span data-stu-id="91d82-191">**ScreenSaverActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-192">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="91d82-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-194">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \| ScreenSaveActive ")</span><span class="sxs-lookup"><span data-stu-id="91d82-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveActive")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-195">L’économiseur d’écran est actif.</span><span class="sxs-lookup"><span data-stu-id="91d82-195">Screen saver is active.</span></span>

</dd> <dt>

<span data-ttu-id="91d82-196">**ScreenSaverExecutable**</span><span class="sxs-lookup"><span data-stu-id="91d82-196">**ScreenSaverExecutable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d82-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-199">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\SCRNSAVE.EXE de bureau \| »)</span><span class="sxs-lookup"><span data-stu-id="91d82-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|SCRNSAVE.EXE")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-200">Nom du fichier exécutable de l’économiseur d’écran actuel.</span><span class="sxs-lookup"><span data-stu-id="91d82-200">Name of the current screen saver executable file.</span></span>

<span data-ttu-id="91d82-201">Exemple : «LOGON. SCR</span><span class="sxs-lookup"><span data-stu-id="91d82-201">Example: "LOGON.SCR"</span></span>

</dd> <dt>

<span data-ttu-id="91d82-202">**ScreenSaverSecure**</span><span class="sxs-lookup"><span data-stu-id="91d82-202">**ScreenSaverSecure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-203">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="91d82-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-205">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \| ScreenSaverIsSecure ")</span><span class="sxs-lookup"><span data-stu-id="91d82-205">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaverIsSecure")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-206">Le mot de passe est activé pour l’économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="91d82-206">Password is enabled for the screen saver.</span></span>

</dd> <dt>

<span data-ttu-id="91d82-207">**ScreenSaverTimeout**</span><span class="sxs-lookup"><span data-stu-id="91d82-207">**ScreenSaverTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-208">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91d82-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-210">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \| ScreenSaveTimeOut "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" seconds ")</span><span class="sxs-lookup"><span data-stu-id="91d82-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-211">Durée écoulée avant le démarrage de l’économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="91d82-211">Amount of time that passes before the screen saver starts.</span></span>

</dd> <dt>

<span data-ttu-id="91d82-212">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="91d82-212">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d82-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-215">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="91d82-215">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91d82-216">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="91d82-216">Identifier by which the current object is known.</span></span>

<span data-ttu-id="91d82-217">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="91d82-217">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d82-218">**Papier peint**</span><span class="sxs-lookup"><span data-stu-id="91d82-218">**Wallpaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d82-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-221">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ \| Papier peint du bureau ")</span><span class="sxs-lookup"><span data-stu-id="91d82-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Wallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-222">Nom de fichier pour la conception du papier peint sur l’arrière-plan du bureau.</span><span class="sxs-lookup"><span data-stu-id="91d82-222">File name for the wallpaper design on the background of the desktop.</span></span>

<span data-ttu-id="91d82-223">Exemple : « WINNT.BMP »</span><span class="sxs-lookup"><span data-stu-id="91d82-223">Example: "WINNT.BMP"</span></span>

</dd> <dt>

<span data-ttu-id="91d82-224">**WallpaperStretched**</span><span class="sxs-lookup"><span data-stu-id="91d82-224">**WallpaperStretched**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-225">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="91d82-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-227">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \| WallpaperStyle ")</span><span class="sxs-lookup"><span data-stu-id="91d82-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|WallpaperStyle")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-228">Le papier peint est étiré pour remplir tout l’écran.</span><span class="sxs-lookup"><span data-stu-id="91d82-228">Wallpaper is stretched to fill the entire screen.</span></span> <span data-ttu-id="91d82-229">Microsoft plus !</span><span class="sxs-lookup"><span data-stu-id="91d82-229">Microsoft Plus!</span></span> <span data-ttu-id="91d82-230">doit être installé pour que cette option soit disponible.</span><span class="sxs-lookup"><span data-stu-id="91d82-230">must be installed before this option is available.</span></span> <span data-ttu-id="91d82-231">Si la **valeur est false**, le papier peint conserve ses dimensions d’origine sur l’arrière-plan du bureau.</span><span class="sxs-lookup"><span data-stu-id="91d82-231">If **FALSE**, the wallpaper retains its original dimensions on the desktop background.</span></span>

</dd> <dt>

<span data-ttu-id="91d82-232">**WallpaperTiled**</span><span class="sxs-lookup"><span data-stu-id="91d82-232">**WallpaperTiled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d82-233">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="91d82-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91d82-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d82-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d82-235">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Panneau de configuration par défaut \\ \\ \\ \\ Desktop \| TileWallpaper ")</span><span class="sxs-lookup"><span data-stu-id="91d82-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|TileWallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="91d82-236">Le papier peint est en mosaïque ou centré.</span><span class="sxs-lookup"><span data-stu-id="91d82-236">Wallpaper is tiled or centered.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91d82-237">Notes</span><span class="sxs-lookup"><span data-stu-id="91d82-237">Remarks</span></span>

<span data-ttu-id="91d82-238">La **classe \_ Bureau Win32** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="91d82-238">The **Win32\_Desktop** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="91d82-239">Le processus appelant qui utilise cette classe doit avoir le privilège **se \_ Restore \_ Name** sur l’ordinateur où se trouve le registre.</span><span class="sxs-lookup"><span data-stu-id="91d82-239">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="91d82-240">Par exemple, si vous énumérez cette classe sur l’ordinateur local, le compte sous lequel votre application s’exécute doit disposer de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="91d82-240">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="91d82-241">Pour plus d’informations, consultez [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="91d82-241">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="91d82-242">Exemples</span><span class="sxs-lookup"><span data-stu-id="91d82-242">Examples</span></span>

<span data-ttu-id="91d82-243">L’exemple de code suivant décrit comment récupérer des informations sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="91d82-243">The following code sample describes how to retrieve desktop information.</span></span>


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



## <a name="requirements"></a><span data-ttu-id="91d82-244">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91d82-244">Requirements</span></span>



| <span data-ttu-id="91d82-245">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91d82-245">Requirement</span></span> | <span data-ttu-id="91d82-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="91d82-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91d82-247">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91d82-247">Minimum supported client</span></span><br/> | <span data-ttu-id="91d82-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91d82-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91d82-249">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91d82-249">Minimum supported server</span></span><br/> | <span data-ttu-id="91d82-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91d82-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91d82-251">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="91d82-251">Namespace</span></span><br/>                | <span data-ttu-id="91d82-252">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="91d82-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="91d82-253">MOF</span><span class="sxs-lookup"><span data-stu-id="91d82-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91d82-254"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91d82-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="91d82-255">DLL</span><span class="sxs-lookup"><span data-stu-id="91d82-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91d82-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91d82-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91d82-257">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91d82-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d82-258">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="91d82-258">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="91d82-259">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91d82-259">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

