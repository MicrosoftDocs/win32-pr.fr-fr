---
description: Si vous choisissez d’implémenter l’effacement dans votre application à l’aide de l’objet InkOverlay, vous pouvez le faire à l’aide de l’une des deux méthodes suivantes.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Effacement à l’aide du stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393520"
---
# <a name="erasing-by-using-the-pen"></a><span data-ttu-id="4fac8-103">Effacement à l’aide du stylet</span><span class="sxs-lookup"><span data-stu-id="4fac8-103">Erasing by Using the Pen</span></span>

<span data-ttu-id="4fac8-104">Si vous choisissez d’implémenter l’effacement dans votre application à l’aide de l’objet [**InkOverlay**](inkoverlay-class.md) , vous pouvez le faire à l’aide de l’une des deux méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4fac8-104">If you choose to implement erasing in your application other than by using the [**InkOverlay**](inkoverlay-class.md) object, you can do so by using one of the following two methods.</span></span>

## <a name="using-the-tip-of-the-pen"></a><span data-ttu-id="4fac8-105">Utilisation de l’info-bulle du stylet</span><span class="sxs-lookup"><span data-stu-id="4fac8-105">Using the Tip of the Pen</span></span>

<span data-ttu-id="4fac8-106">La pointe du stylet est généralement utilisée pour l’écriture manuscrite et le dessin. Toutefois, le Conseil peut également être utilisé pour effacer l’encre.</span><span class="sxs-lookup"><span data-stu-id="4fac8-106">The tip of the tablet pen is generally used for handwriting and drawing; however, the tip can also be used to erase ink.</span></span> <span data-ttu-id="4fac8-107">Pour ce faire, l’application doit disposer d’un mode d’effacement que les utilisateurs peuvent employer.</span><span class="sxs-lookup"><span data-stu-id="4fac8-107">To do so, the application must have an erase mode that users can employ.</span></span> <span data-ttu-id="4fac8-108">Dans ce mode, utilisez le test de positionnement pour déterminer l’encre sur laquelle le curseur est déplacé.</span><span class="sxs-lookup"><span data-stu-id="4fac8-108">In this mode, use hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="4fac8-109">Vous pouvez définir le mode d’effacement pour supprimer uniquement l’encre sur laquelle le curseur passe ou les traits entiers qui croisent le chemin d’accès du curseur, en fonction de la conception ou des considérations fonctionnelles.</span><span class="sxs-lookup"><span data-stu-id="4fac8-109">You can set the erase mode to delete only the ink that the cursor passes over or whole strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="4fac8-110">Pour obtenir un exemple d’utilisation d’un mode d’effacement pour effacer l’encre, consultez l’exemple d’effacement d' [encre](ink-erasing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4fac8-110">For an example of how to use an erase mode to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

## <a name="using-the-top-of-the-pen"></a><span data-ttu-id="4fac8-111">En utilisant le haut du stylet</span><span class="sxs-lookup"><span data-stu-id="4fac8-111">Using the Top of the Pen</span></span>

<span data-ttu-id="4fac8-112">Pour implémenter l’effacement avec le haut du stylet du Tablet PC, votre application doit rechercher une modification dans le curseur.</span><span class="sxs-lookup"><span data-stu-id="4fac8-112">To implement erasing with the top of the tablet pen, your application must look for a change in the cursor.</span></span> <span data-ttu-id="4fac8-113">Pour rechercher le curseur inversé, écoutez l’événement [**CursorInRange**](inkoverlay-cursorinrange.md) pour déterminer quand le curseur se trouve dans le contexte de votre application.</span><span class="sxs-lookup"><span data-stu-id="4fac8-113">To look for the inverted cursor, listen for the [**CursorInRange**](inkoverlay-cursorinrange.md) event to determine when the cursor is within the context of your application.</span></span> <span data-ttu-id="4fac8-114">Lorsque le curseur se trouve dans la plage, recherchez la propriété [**inversée**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) sur l’objet [**curseur**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="4fac8-114">When the cursor is in range, look for the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span> <span data-ttu-id="4fac8-115">Si la propriété **inversée** a la **valeur true**, effectuez un test de positionnement pour déterminer l’encre sur laquelle le curseur est déplacé.</span><span class="sxs-lookup"><span data-stu-id="4fac8-115">If the **Inverted** property is **true**, perform hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="4fac8-116">Effacez l’encre ou les traits qui croisent le chemin d’accès du curseur, en fonction de la conception ou des considérations fonctionnelles.</span><span class="sxs-lookup"><span data-stu-id="4fac8-116">Erase either the ink or the strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="4fac8-117">Pour obtenir un exemple d’utilisation du haut du stylet pour effacer l’encre, consultez l' [exemple d’effacement d’encre](ink-erasing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4fac8-117">For an example of how to use the top of the pen to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a><span data-ttu-id="4fac8-118">Détermination de l’activation de l’effacement avec le haut du stylet</span><span class="sxs-lookup"><span data-stu-id="4fac8-118">Determining if Erasing with the Top of the Pen Is Enabled</span></span>

<span data-ttu-id="4fac8-119">Les utilisateurs peuvent utiliser le haut du stylet pour effacer l’encre dans les applications conçues pour Tablet PC, si leur matériel spécifique le permet.</span><span class="sxs-lookup"><span data-stu-id="4fac8-119">Users can use the top of the pen to erase ink in applications designed for Tablet PC, if their particular hardware allows for it.</span></span> <span data-ttu-id="4fac8-120">Cette fonctionnalité est accessible par une case à cocher dans la zone de groupe boutons du stylet sous l’onglet Options du stylet de la boîte de dialogue Paramètres du Tablet PC et du stylet.</span><span class="sxs-lookup"><span data-stu-id="4fac8-120">This functionality is accessed by a check box in the Pen buttons group box on the Pen Options tab of the Tablet and Pen Settings control panel dialog.</span></span> <span data-ttu-id="4fac8-121">Pour déterminer si l’utilisateur a activé l’effacement pour le haut du stylet, vérifiez la sous-clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="4fac8-121">To detect if the user has enabled erasing for the top of the pen, check the following registry subkey:</span></span>

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

<span data-ttu-id="4fac8-122">L' `EraseEnable` entrée de cette sous-clé est de type **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="4fac8-122">The `EraseEnable` entry of this subkey is of type **REG\_DWORD**.</span></span> <span data-ttu-id="4fac8-123">La valeur de cette entrée est 1 pour activé, ou 0 pour désactivé.</span><span class="sxs-lookup"><span data-stu-id="4fac8-123">The value of this entry is 1 for enabled, or 0 for disabled.</span></span> <span data-ttu-id="4fac8-124">Les autres valeurs sont réservées pour un usage ultérieur.</span><span class="sxs-lookup"><span data-stu-id="4fac8-124">Other values are reserved for future use.</span></span>

<span data-ttu-id="4fac8-125">Si votre application autorise l’utilisation du haut du stylet pour l’effacement, vous devez vérifier et mettre en cache la valeur de l’entrée EraseEnable dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="4fac8-125">If your application allows the top of the pen to be used for erasing, you should check and cache the value of the EraseEnable entry when:</span></span>

-   <span data-ttu-id="4fac8-126">Votre application démarre.</span><span class="sxs-lookup"><span data-stu-id="4fac8-126">Your application launches.</span></span>
-   <span data-ttu-id="4fac8-127">Chaque fois que votre application reçoit le focus après avoir perdu le focus.</span><span class="sxs-lookup"><span data-stu-id="4fac8-127">Any time your application receives focus after losing focus.</span></span>

<span data-ttu-id="4fac8-128">Utilisez cette valeur mise en cache pour modifier le comportement de votre application de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="4fac8-128">Use this cached value to modify the behavior of your application appropriately.</span></span>

<span data-ttu-id="4fac8-129">L’exemple C suivant \# définit une `GetEraseEnabled` méthode qui vérifie la valeur de l' `EraseEnable` entrée de la `SysEventParameters` sous-clé.</span><span class="sxs-lookup"><span data-stu-id="4fac8-129">The following C\# example defines a `GetEraseEnabled` method that checks the value of the `EraseEnable` entry of the `SysEventParameters` subkey.</span></span> <span data-ttu-id="4fac8-130">La `GetEraseEnabled` méthode retourne **true** si la valeur de l’entrée est 1 ; retourne **false** si la valeur de l’entrée est 0, ou lève une [exception InvalidOperationException](/dotnet/api/system.invalidoperationexception) si la valeur de l’entrée est différente de 1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="4fac8-130">The `GetEraseEnabled` method returns **TRUE** if the value of the entry is 1; returns **FALSE** if the value of the entry is 0; or throws an [InvalidOperationException](/dotnet/api/system.invalidoperationexception) exception if the value of the entry is other than 1 or 0.</span></span> <span data-ttu-id="4fac8-131">La `GetEraseEnabled` méthode retourne la valeur attendue **true** si la sous-clé ou l’entrée n’est pas présente.</span><span class="sxs-lookup"><span data-stu-id="4fac8-131">The `GetEraseEnabled` method returns the expected value of **TRUE** if either the subkey or the entry is not present.</span></span>


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
