---
description: Ajoute un nouveau canal à la liste de canaux dans le menu Favoris de Windows Internet Explorer et à la barre de canaux sur le bureau.
title: Méthode ShellUIHelper. AddChannel (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: 93c62abd8f788f950e36bcfc5fa10f7c991a6410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991793"
---
# <a name="shelluihelperaddchannel-method"></a><span data-ttu-id="6b024-103">Méthode ShellUIHelper. AddChannel</span><span class="sxs-lookup"><span data-stu-id="6b024-103">ShellUIHelper.AddChannel method</span></span>

<span data-ttu-id="6b024-104">Ajoute un nouveau canal à la liste de canaux dans le menu **favoris** de Windows Internet Explorer et à la barre de **canaux** sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="6b024-104">Adds a new channel to the list of channels in the Windows Internet Explorer **Favorites** menu and to the **Channel** bar on the desktop.</span></span>

> [!Note]  
> <span data-ttu-id="6b024-105">Cette méthode n’est plus prise en charge sous Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6b024-105">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="6b024-106">Dans ce système d’exploitation, il renvoie E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="6b024-106">Under that operating system, it returns E\_NOTIMPL.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6b024-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b024-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="6b024-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b024-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b024-109">*surl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b024-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b024-110">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6b024-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6b024-111">Valeur de **chaîne** qui spécifie l’URL du fichier CDF.</span><span class="sxs-lookup"><span data-stu-id="6b024-111">A **String** value that specifies the URL of the CDF file.</span></span>

> [!Note]  
> <span data-ttu-id="6b024-112">Les liens contenus dans le fichier CDF doivent utiliser des protocoles HTTP, HTTPs ou FTP.</span><span class="sxs-lookup"><span data-stu-id="6b024-112">The links in the CDF file must use HTTP, HTTPS, or FTP protocols.</span></span> <span data-ttu-id="6b024-113">Si le fichier CDF contient un autre protocole, l’ajout du canal échoue et aucune boîte de dialogue ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6b024-113">If the CDF file contains any other protocol, the addition of the channel fails and no dialog box appears.</span></span>

 

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="6b024-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="6b024-114">Examples</span></span>

<span data-ttu-id="6b024-115">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript Embedded en HTML et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6b024-115">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="6b024-116">Langage</span><span class="sxs-lookup"><span data-stu-id="6b024-116">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



<span data-ttu-id="6b024-117">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="6b024-117">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6b024-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6b024-118">Requirements</span></span>



| <span data-ttu-id="6b024-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b024-119">Requirement</span></span> | <span data-ttu-id="6b024-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b024-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b024-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b024-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6b024-122">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b024-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6b024-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b024-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6b024-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b024-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6b024-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b024-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b024-126"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b024-126"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="6b024-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6b024-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b024-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="6b024-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
