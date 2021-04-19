---
description: Vous pouvez masquer le bouton Annuler qui est utilisé pour annuler une installation à l’aide d’une option de ligne de commande, de l’API Windows Installer ou d’une action personnalisée. Le bouton Annuler peut être masqué pour tout ou partie de l’installation, en fonction de la méthode que vous utilisez.
ms.assetid: de2bb788-0d19-4818-8038-cae6000b38c4
title: Masquage du bouton Annuler pendant une installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e55658bc69fe81b83b13d6c6ee7da84db77ad466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529282"
---
# <a name="hiding-the-cancel-button-during-an-installation"></a><span data-ttu-id="69f7c-104">Masquage du bouton Annuler pendant une installation</span><span class="sxs-lookup"><span data-stu-id="69f7c-104">Hiding the Cancel Button During an Installation</span></span>

<span data-ttu-id="69f7c-105">Vous pouvez masquer le bouton **Annuler** qui est utilisé pour annuler une installation à l’aide d’une option de ligne de commande, de l’API Windows Installer ou d’une action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="69f7c-105">You can hide the **Cancel** button that is used to cancel an installation by using a command-line option, the Windows Installer API, or a custom action.</span></span> <span data-ttu-id="69f7c-106">Le bouton **Annuler** peut être masqué pour tout ou partie de l’installation, en fonction de la méthode que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="69f7c-106">The **Cancel** button can be hidden for part or all of the installation depending on which method you use.</span></span>

## <a name="hiding-the-cancel-button-from-the-command-line"></a><span data-ttu-id="69f7c-107">Masquage du bouton Annuler à partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="69f7c-107">Hiding the Cancel Button from the Command Line</span></span>

<span data-ttu-id="69f7c-108">Le bouton **Annuler** peut être masqué lors de l’installation à l’aide de l’option de ligne de commande ( !).</span><span class="sxs-lookup"><span data-stu-id="69f7c-108">The **Cancel** button can be hidden during installation by using the (!) command-line option.</span></span> <span data-ttu-id="69f7c-109">Cette opération ne peut être effectuée que pour une installation de base au niveau de l’interface utilisateur (/QB).</span><span class="sxs-lookup"><span data-stu-id="69f7c-109">This can only be done for a basic user interface level installation (/qb).</span></span> <span data-ttu-id="69f7c-110">Le bouton **Annuler** est masqué pour l’ensemble de l’installation.</span><span class="sxs-lookup"><span data-stu-id="69f7c-110">The **Cancel** button is hidden for the entire installation.</span></span> <span data-ttu-id="69f7c-111">Pour plus d’informations, consultez [options de ligne de commande](command-line-options.md) et niveaux d' [interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="69f7c-111">For more information, see [Command-Line Options](command-line-options.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="69f7c-112">La ligne de commande suivante masque le bouton **Annuler** et installe Example.msi.</span><span class="sxs-lookup"><span data-stu-id="69f7c-112">The following command line hides the **Cancel** button and installs Example.msi.</span></span>

<span data-ttu-id="69f7c-113">**msiexec/I example.msi/QB !**</span><span class="sxs-lookup"><span data-stu-id="69f7c-113">**msiexec /I example.msi /qb!**</span></span>

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a><span data-ttu-id="69f7c-114">Masquage du bouton Annuler d’une application ou d’un script</span><span class="sxs-lookup"><span data-stu-id="69f7c-114">Hiding the Cancel Button from an Application or Script</span></span>

<span data-ttu-id="69f7c-115">Vous pouvez écrire une application ou un script pour masquer le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="69f7c-115">You can write an application or script to hide the **Cancel** button.</span></span> <span data-ttu-id="69f7c-116">Cette opération ne peut être effectuée que pour une installation de base au niveau de l’interface utilisateur, de sorte que le bouton **Annuler** est masqué pour l’ensemble de l’installation.</span><span class="sxs-lookup"><span data-stu-id="69f7c-116">This can only be done for a basic UI level installation so that the **Cancel** button is hidden for the entire installation.</span></span>

<span data-ttu-id="69f7c-117">Pour masquer le bouton Annuler d’une application, définissez INSTALLUILEVEL \_ HIDECANCEL lors de l’appel de [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="69f7c-117">To hide the Cancel button from an application, set INSTALLUILEVEL\_HIDECANCEL when calling [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="69f7c-118">L’exemple suivant masque le bouton **Annuler** et installe Example.msi.</span><span class="sxs-lookup"><span data-stu-id="69f7c-118">The following example hides the **Cancel** button and installs Example.msi.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")

int main()  
{

INSTALLUILEVEL uiPrevLevel = MsiSetInternalUI( INSTALLUILEVEL(INSTALLUILEVEL_BASIC | INSTALLUILEVEL_HIDECANCEL), 0); 
UINT uiStat = MsiInstallProduct(_T("example.msi"), NULL);

return 0;  
}
```



<span data-ttu-id="69f7c-119">Pour masquer le bouton **Annuler** du script, ajoutez msiUILevelHideCancel à la propriété [**UILevel**](installer-uilevel.md) de l' [**objet installer**](installer-object.md).</span><span class="sxs-lookup"><span data-stu-id="69f7c-119">To hide the **Cancel** button from script, add msiUILevelHideCancel to the [**UILevel**](installer-uilevel.md) property of the [**Installer Object**](installer-object.md).</span></span> <span data-ttu-id="69f7c-120">L’exemple VBScript suivant masque le bouton **Annuler** et installe Example.msi.</span><span class="sxs-lookup"><span data-stu-id="69f7c-120">The following VBScript sample hides the **Cancel** button and installs Example.msi.</span></span>


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a><span data-ttu-id="69f7c-121">Masquage du bouton Annuler pour les parties d’une installation à l’aide d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="69f7c-121">Hiding the Cancel Button for Parts of an Installation Using a Custom Action</span></span>

<span data-ttu-id="69f7c-122">Votre installation peut masquer et afficher le bouton **Annuler** pendant les parties d’une installation en envoyant un \_ message INSTALLMESSAGE COMMONDATA à l’aide d’un script ou d’une action personnalisée dll.</span><span class="sxs-lookup"><span data-stu-id="69f7c-122">Your installation can hide and unhide the **Cancel** button during parts of an installation by sending an INSTALLMESSAGE\_COMMONDATA message using a DLL custom action or scripts.</span></span> <span data-ttu-id="69f7c-123">Pour plus d’informations, consultez [bibliothèques de liens dynamiques](dynamic-link-libraries.md), [scripts](scripts.md), [actions personnalisées](custom-actions.md)et [envoi de messages à Windows Installer à l’aide de MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="69f7c-123">For more information, see [Dynamic-Link Libraries](dynamic-link-libraries.md), [Scripts](scripts.md), [Custom Actions](custom-actions.md), and [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="69f7c-124">Un appel à une action personnalisée doit fournir un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="69f7c-124">A call to a custom action must provide a record.</span></span> <span data-ttu-id="69f7c-125">Le champ 1 de cet enregistrement doit contenir la valeur 2 (deux) pour spécifier le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="69f7c-125">Field 1 of this record must contain the value 2 (two) to specify the **Cancel** button.</span></span> <span data-ttu-id="69f7c-126">Le champ 2 doit contenir la valeur 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="69f7c-126">Field 2 must contain either the value 0 or 1.</span></span> <span data-ttu-id="69f7c-127">La valeur 0 dans le champ 2 masque le bouton et la valeur 1 dans le champ 2 affiche le bouton.</span><span class="sxs-lookup"><span data-stu-id="69f7c-127">A value of 0 in Field 2 hides the button and a value of 1 in Field 2 unhides the button.</span></span> <span data-ttu-id="69f7c-128">Notez que l’allocation d’un enregistrement de taille 2 avec [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) fournit les champs 0, 1 et 2.</span><span class="sxs-lookup"><span data-stu-id="69f7c-128">Note that allocating a record of size 2 with [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) provides fields 0, 1, and 2.</span></span>

<span data-ttu-id="69f7c-129">L’exemple d’action personnalisée de DLL suivant masque le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="69f7c-129">The following sample DLL custom action hides the **Cancel** button.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>

UINT __stdcall HideCancelButton(MSIHANDLE hInstall)
{
    PMSIHANDLE hRecord = MsiCreateRecord(2);
    if ( !hRecord)
        return ERROR_INSTALL_FAILURE;

    if (ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 1, 2)
     || ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 2, 0))
        return ERROR_INSTALL_FAILURE;

    MsiProcessMessage(hInstall, INSTALLMESSAGE_COMMONDATA, hRecord);

    return ERROR_SUCCESS;
}
```



<span data-ttu-id="69f7c-130">L’action personnalisée VBScript suivante masque le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="69f7c-130">The following VBScript Custom Action hides the **Cancel** button.</span></span>


```VB
Function HideCancelButton()

    Dim Record
    Set Record = Installer.CreateRecord(2)

    Record.IntegerData(1) = 2
    Record.IntegerData(2) = 0

    Session.Message msiMessageTypeCommonData, Record
 
    ' return success
    HideCancelButton = 1
    Exit Function

End Function
```



 

 



