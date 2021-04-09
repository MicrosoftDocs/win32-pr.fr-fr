---
description: La fonction DocumentProperties récupère ou modifie les informations d’initialisation de l’imprimante ou affiche une feuille de propriétés de configuration de l’imprimante pour l’imprimante spécifiée.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: Fonction DocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 732cb6901b444117d0599a2899327ebcb749cf74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115794"
---
# <a name="documentproperties-function"></a><span data-ttu-id="ce627-103">Fonction DocumentProperties</span><span class="sxs-lookup"><span data-stu-id="ce627-103">DocumentProperties function</span></span>

<span data-ttu-id="ce627-104">La fonction **DocumentProperties** récupère ou modifie les informations d’initialisation de l’imprimante ou affiche une feuille de propriétés de configuration de l’imprimante pour l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ce627-104">The **DocumentProperties** function retrieves or modifies printer initialization information or displays a printer-configuration property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce627-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce627-105">Syntax</span></span>


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a><span data-ttu-id="ce627-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce627-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce627-107">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce627-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce627-108">Handle de la fenêtre parente de la feuille de propriétés de configuration de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce627-108">A handle to the parent window of the printer-configuration property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="ce627-109">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce627-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce627-110">Handle d’un objet Printer.</span><span class="sxs-lookup"><span data-stu-id="ce627-110">A handle to a printer object.</span></span> <span data-ttu-id="ce627-111">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce627-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="ce627-112">*pDeviceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce627-112">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce627-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’appareil pour lequel la feuille de propriétés de configuration de l’imprimante est affichée.</span><span class="sxs-lookup"><span data-stu-id="ce627-113">A pointer to a null-terminated string that specifies the name of the device for which the printer-configuration property sheet is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="ce627-114">*pDevModeOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ce627-114">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce627-115">Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui reçoit les données de configuration d’imprimante spécifiées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce627-115">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that receives the printer configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="ce627-116">*pDevModeInput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce627-116">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce627-117">Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que le système d’exploitation utilise pour initialiser les contrôles de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ce627-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that the operating system uses to initialize the property sheet controls.</span></span>

<span data-ttu-id="ce627-118">Ce paramètre est utilisé uniquement si l’indicateur **DM \_ dans la \_ mémoire tampon** est défini dans le paramètre *fMode* .</span><span class="sxs-lookup"><span data-stu-id="ce627-118">This parameter is only used if the **DM\_IN\_BUFFER** flag is set in the *fMode* parameter.</span></span> <span data-ttu-id="ce627-119">Si **DM \_ dans la \_ mémoire tampon** n’est pas défini, le système d’exploitation utilise le [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)par défaut de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce627-119">If **DM\_IN\_BUFFER** is not set, the operating system uses the printer's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span>

</dd> <dt>

<span data-ttu-id="ce627-120">*fMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce627-120">*fMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce627-121">Opérations exécutées par la fonction.</span><span class="sxs-lookup"><span data-stu-id="ce627-121">The operations the function performs.</span></span> <span data-ttu-id="ce627-122">Si ce paramètre est égal à zéro, la fonction **DocumentProperties** retourne le nombre d’octets requis par la structure de données [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) du pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce627-122">If this parameter is zero, the **DocumentProperties** function returns the number of bytes required by the printer driver's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure.</span></span> <span data-ttu-id="ce627-123">Sinon, utilisez une ou plusieurs des constantes suivantes pour construire une valeur pour ce paramètre. Notez, toutefois, que pour modifier les paramètres d’impression, une application doit spécifier au moins une valeur d’entrée et une valeur de sortie.</span><span class="sxs-lookup"><span data-stu-id="ce627-123">Otherwise, use one or more of the following constants to construct a value for this parameter; note, however, that in order to change the print settings, an application must specify at least one input value and one output value.</span></span>



| <span data-ttu-id="ce627-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce627-124">Value</span></span>                                                                                                                                                          | <span data-ttu-id="ce627-125">Signification</span><span class="sxs-lookup"><span data-stu-id="ce627-125">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <span data-ttu-id="ce627-126"><dt>**DM \_ dans la \_ mémoire tampon**</dt></span><span class="sxs-lookup"><span data-stu-id="ce627-126"><dt>**DM\_IN\_BUFFER**</dt></span></span> </dl>    | <span data-ttu-id="ce627-127">Valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ce627-127">Input value.</span></span> <span data-ttu-id="ce627-128">Avant de demander, de copier ou de mettre à jour, la fonction fusionne les paramètres d’impression actuels du pilote d’imprimante avec les paramètres de la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) spécifiée par le paramètre *pDevModeInput* .</span><span class="sxs-lookup"><span data-stu-id="ce627-128">Before prompting, copying, or updating, the function merges the printer driver's current print settings with the settings in the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure specified by the *pDevModeInput* parameter.</span></span> <span data-ttu-id="ce627-129">La fonction met à jour la structure uniquement pour les membres spécifiés par le membre **dmFields** de la structure **DEVMODE** .</span><span class="sxs-lookup"><span data-stu-id="ce627-129">The function updates the structure only for those members specified by the **DEVMODE** structure's **dmFields** member.</span></span> <span data-ttu-id="ce627-130">Cette valeur est également définie en tant que **\_ modification DM**.</span><span class="sxs-lookup"><span data-stu-id="ce627-130">This value is also defined as **DM\_MODIFY**.</span></span> <span data-ttu-id="ce627-131">En cas de conflit pendant la fusion, les paramètres de la structure **DEVMODE** spécifiée par *pDevModeInput* remplacent les paramètres d’impression actuels du pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce627-131">In cases of conflict during the merge, the settings in the **DEVMODE** structure specified by *pDevModeInput* override the printer driver's current print settings.</span></span><br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <span data-ttu-id="ce627-132"><dt>**DM \_ dans l' \_ invite**</dt></span><span class="sxs-lookup"><span data-stu-id="ce627-132"><dt>**DM\_IN\_PROMPT**</dt></span></span> </dl>    | <span data-ttu-id="ce627-133">Valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ce627-133">Input value.</span></span> <span data-ttu-id="ce627-134">La fonction affiche la feuille de propriétés configuration de l’impression du pilote d’imprimante, puis modifie les paramètres de la structure de données [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) de l’imprimante en fonction des valeurs spécifiées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce627-134">The function presents the printer driver's Print Setup property sheet and then changes the settings in the printer's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure to those values specified by the user.</span></span> <span data-ttu-id="ce627-135">Cette valeur est également définie en tant qu' **\_ invite DM**.</span><span class="sxs-lookup"><span data-stu-id="ce627-135">This value is also defined as **DM\_PROMPT**.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <span data-ttu-id="ce627-136"><dt>**\_mémoire tampon de sortie DM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce627-136"><dt>**DM\_OUT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="ce627-137">Valeur de sortie.</span><span class="sxs-lookup"><span data-stu-id="ce627-137">Output value.</span></span> <span data-ttu-id="ce627-138">La fonction écrit les paramètres d’impression actuels du pilote d’imprimante, y compris les données privées, dans la structure de données [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) spécifiée par le paramètre *pDevModeOutput* .</span><span class="sxs-lookup"><span data-stu-id="ce627-138">The function writes the printer driver's current print settings, including private data, to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure specified by the *pDevModeOutput* parameter.</span></span> <span data-ttu-id="ce627-139">L’appelant doit allouer une mémoire tampon suffisamment grande pour contenir les informations.</span><span class="sxs-lookup"><span data-stu-id="ce627-139">The caller must allocate a buffer sufficiently large to contain the information.</span></span> <span data-ttu-id="ce627-140">Si les jeux **de \_ \_ mémoires tampons** de bits DM sont clairs, le paramètre *PDevModeOutput* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ce627-140">If the bit **DM\_OUT\_BUFFER** sets is clear, the *pDevModeOutput* parameter can be **NULL**.</span></span> <span data-ttu-id="ce627-141">Cette valeur est également définie en tant que **\_ copie DM**.</span><span class="sxs-lookup"><span data-stu-id="ce627-141">This value is also defined as **DM\_COPY**.</span></span><br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce627-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce627-142">Return value</span></span>

<span data-ttu-id="ce627-143">Si le paramètre *fMode* est égal à zéro, la valeur de retour correspond à la taille de la mémoire tampon requise pour contenir les données d’initialisation du pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce627-143">If the *fMode* parameter is zero, the return value is the size of the buffer required to contain the printer driver initialization data.</span></span> <span data-ttu-id="ce627-144">Notez que cette mémoire tampon peut être plus grande qu’une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) si le pilote d’imprimante ajoute des données privées à la structure.</span><span class="sxs-lookup"><span data-stu-id="ce627-144">Note that this buffer can be larger than a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure if the printer driver appends private data to the structure.</span></span>

<span data-ttu-id="ce627-145">Si la fonction affiche la feuille de propriétés, la valeur de retour est **IDOK** ou **IDCANCEL**, selon le bouton sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce627-145">If the function displays the property sheet, the return value is either **IDOK** or **IDCANCEL**, depending on which button the user selects.</span></span>

<span data-ttu-id="ce627-146">Si la fonction n’affiche pas la feuille de propriétés et réussit, la valeur de retour est **IDOK**.</span><span class="sxs-lookup"><span data-stu-id="ce627-146">If the function does not display the property sheet and is successful, the return value is **IDOK**.</span></span>

<span data-ttu-id="ce627-147">Si la fonction échoue, la valeur de retour est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="ce627-147">If the function fails, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce627-148">Notes</span><span class="sxs-lookup"><span data-stu-id="ce627-148">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ce627-149">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ce627-149">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ce627-150">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="ce627-150">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ce627-151">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="ce627-151">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ce627-152">La chaîne vers laquelle pointe le paramètre *pDeviceName* peut être obtenue en appelant la fonction [**GetPrinter**](getprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="ce627-152">The string pointed to by the *pDeviceName* parameter can be obtained by calling the [**GetPrinter**](getprinter.md) function.</span></span>

<span data-ttu-id="ce627-153">La structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) réellement utilisée par un pilote d’imprimante contient la partie indépendante du périphérique (telle que définie ci-dessus), suivie d’une partie spécifique au pilote qui varie en fonction de la taille et du contenu avec chaque pilote et chaque version du pilote.</span><span class="sxs-lookup"><span data-stu-id="ce627-153">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure actually used by a printer driver contains the device-independent part (as defined above) followed by a driver-specific part that varies in size and content with each driver and driver version.</span></span> <span data-ttu-id="ce627-154">En raison de la dépendance de ce pilote, il est très important pour les applications d’interroger le pilote sur la taille correcte de la structure **DEVMODE** avant d’allouer une mémoire tampon pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ce627-154">Because of this driver dependence, it is very important for applications to query the driver for the correct size of the **DEVMODE** structure before allocating a buffer for it.</span></span>

<span data-ttu-id="ce627-155">**Pour apporter des modifications aux paramètres d’impression locaux d’une application, une application doit suivre les étapes suivantes :**</span><span class="sxs-lookup"><span data-stu-id="ce627-155">**To make changes to print settings that are local to an application, an application should follow these steps:**</span></span>

1.  <span data-ttu-id="ce627-156">Obtient le nombre d’octets requis pour la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) complète en appelant **DocumentProperties** et en spécifiant zéro dans le paramètre *fMode* .</span><span class="sxs-lookup"><span data-stu-id="ce627-156">Get the number of bytes required for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure by calling **DocumentProperties** and specifying zero in the *fMode* parameter.</span></span>
2.  <span data-ttu-id="ce627-157">Allouez de la mémoire pour la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) complète.</span><span class="sxs-lookup"><span data-stu-id="ce627-157">Allocate memory for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
3.  <span data-ttu-id="ce627-158">Obtient les paramètres actuels de l’imprimante en appelant **DocumentProperties**.</span><span class="sxs-lookup"><span data-stu-id="ce627-158">Get the current printer settings by calling **DocumentProperties**.</span></span> <span data-ttu-id="ce627-159">Transmettez un pointeur vers la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) allouée à l’étape 2 en tant que paramètre *pDevModeOutput* et spécifiez la valeur du **\_ \_ tampon de sortie DM** .</span><span class="sxs-lookup"><span data-stu-id="ce627-159">Pass a pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure allocated in Step 2 as the *pDevModeOutput* parameter and specify the **DM\_OUT\_BUFFER** value.</span></span>
4.  <span data-ttu-id="ce627-160">Modifiez les membres appropriés de la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retournée et indiquez les membres qui ont été modifiés en définissant les bits correspondants dans le membre **dmFields** du **DEVMODE**.</span><span class="sxs-lookup"><span data-stu-id="ce627-160">Modify the appropriate members of the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure and indicate which members were changed by setting the corresponding bits in the **dmFields** member of the **DEVMODE**.</span></span>
5.  <span data-ttu-id="ce627-161">Appelez **DocumentProperties** et transmettez à nouveau la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) modifiée en tant que paramètres *pDevModeInput* et *pDevModeOutput* et spécifiez les valeurs de **\_ \_ mémoire tampon** **DM \_ dans \_ buffer** et DM out (qui sont combinées à l’aide de l’opérateur or). La structure **DEVMODE** retournée par le troisième appel à **DocumentProperties** peut être utilisée comme argument dans un appel à la fonction [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) .</span><span class="sxs-lookup"><span data-stu-id="ce627-161">Call **DocumentProperties** and pass the modified [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure back as both the *pDevModeInput* and *pDevModeOutput* parameters and specify both the **DM\_IN\_BUFFER** and **DM\_OUT\_BUFFER** values (which are combined using the OR operator).The **DEVMODE** structure returned by the third call to **DocumentProperties** can be used as an argument in a call to the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function.</span></span>

<span data-ttu-id="ce627-162">Pour créer un handle vers un contexte de périphérique d’impression à l’aide des paramètres actuels de l’imprimante, il vous suffit d’appeler **DocumentProperties** à deux reprises, comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="ce627-162">To create a handle to a printer-device context using the current printer settings, you only need to call **DocumentProperties** twice, as described above.</span></span> <span data-ttu-id="ce627-163">Le premier appel obtient la taille du [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) complet et le deuxième appel Initialise le **DEVMODE** avec les paramètres actuels de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce627-163">The first call gets the size of the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) and the second call initializes the **DEVMODE** with the current printer settings.</span></span> <span data-ttu-id="ce627-164">Transmettez le **DEVMODE** initialisé à [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) pour obtenir le handle du contexte de périphérique d’impression.</span><span class="sxs-lookup"><span data-stu-id="ce627-164">Pass the initialized **DEVMODE** to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) to obtain the handle to the printer device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce627-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce627-165">Requirements</span></span>



| <span data-ttu-id="ce627-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce627-166">Requirement</span></span> | <span data-ttu-id="ce627-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce627-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce627-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce627-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ce627-169">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce627-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ce627-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce627-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ce627-171">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce627-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ce627-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce627-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce627-173"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce627-173"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ce627-174">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce627-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce627-175"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce627-175"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ce627-176">DLL</span><span class="sxs-lookup"><span data-stu-id="ce627-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce627-177"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ce627-177"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ce627-178">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="ce627-178">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ce627-179">**DocumentPropertiesW** (Unicode) et **DocumentPropertiesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ce627-179">**DocumentPropertiesW** (Unicode) and **DocumentPropertiesA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="ce627-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce627-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce627-181">Impression</span><span class="sxs-lookup"><span data-stu-id="ce627-181">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ce627-182">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="ce627-182">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ce627-183">**AdvancedDocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="ce627-183">**AdvancedDocumentProperties**</span></span>](advanceddocumentproperties.md)
</dt> <dt>

[<span data-ttu-id="ce627-184">**CreateDC**</span><span class="sxs-lookup"><span data-stu-id="ce627-184">**CreateDC**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[<span data-ttu-id="ce627-185">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="ce627-185">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="ce627-186">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="ce627-186">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="ce627-187">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="ce627-187">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

