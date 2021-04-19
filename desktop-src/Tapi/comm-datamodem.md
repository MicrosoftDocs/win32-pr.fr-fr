---
description: La classe d’appareil comm/datamodem se compose d’appareils datamodem.
ms.assetid: 6bc314c6-30ec-4318-856a-3ab2fa6aadfb
title: comm/datamodem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89210bcf14931e3905f71cdbb8678f5519cc4c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519765"
---
# <a name="commdatamodem"></a><span data-ttu-id="e4fa8-103">comm/datamodem</span><span class="sxs-lookup"><span data-stu-id="e4fa8-103">comm/datamodem</span></span>

<span data-ttu-id="e4fa8-104">La classe d’appareil comm/datamodem se compose d’appareils datamodem.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-104">The comm/datamodem device class consists of datamodem devices.</span></span> <span data-ttu-id="e4fa8-105">Vous accédez à ces appareils à l’aide des [fonctions](/windows/desktop/DevIO/communications-functions)de [fichier](/windows/desktop/FileIO/file-management-functions) et de communication.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-105">You access these devices by using the [file](/windows/desktop/FileIO/file-management-functions) and [communications functions](/windows/desktop/DevIO/communications-functions).</span></span> <span data-ttu-id="e4fa8-106">Les appareils de cette classe sont associés à des appareils de ligne qui prennent en charge le \_ type de média LINEMEDIAMODE DATAMODEM, qui est spécifié dans le membre **dwMediaModes** de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_DATAMODEM media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="e4fa8-107">La fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) remplit une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en affectant à **dwStringFormat** la \_ valeur binaire STRINGFORMAT et en ajoutant les membres supplémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="e4fa8-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to the STRINGFORMAT\_BINARY value and appending these additional members:</span></span>

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

<span data-ttu-id="e4fa8-108">Le membre **hComm** est le descripteur du port de communication ouvert.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-108">The **hComm** member is the handle of the open communications port.</span></span> <span data-ttu-id="e4fa8-109">Ce membre a la valeur **null** si le port n’est pas encore ouvert ou si le paramètre *dwSelect* de [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) n’est pas la valeur de l' \_ appel LINECALLSELECT.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-109">This member is **NULL** if the port is not yet open or if the *dwSelect* parameter of [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) is not the LINECALLSELECT\_CALL value.</span></span> <span data-ttu-id="e4fa8-110">Si un appel est actif, le fournisseur de services ouvre généralement le port lui-même pour contrôler directement le matériel de communication, mais il n’est nécessaire que pour retourner un handle valide si la ligne est connectée.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-110">If a call is active, the service provider typically opens the port itself to get direct control of the communications hardware, but is only required to return a valid handle if the line is connected.</span></span> <span data-ttu-id="e4fa8-111">Le fournisseur de services ouvre le port à l’aide de la \_ valeur de chevauchement de l’indicateur \_ de fichier, puis il configure le port à l’aide des paramètres spécifiés par la fonction [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .</span><span class="sxs-lookup"><span data-stu-id="e4fa8-111">The service provider opens the port using the FILE\_FLAG\_OVERLAPPED value and then configures the port using the settings specified by the [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) function.</span></span> <span data-ttu-id="e4fa8-112">Vous pouvez définir des options de configuration supplémentaires pour l’appareil en utilisant des fonctions de communication avec le handle retourné.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-112">You can set additional configuration options for the device by using communications functions with the returned handle.</span></span>

<span data-ttu-id="e4fa8-113">Le membre **szDeviceName** est une chaîne se terminant par un caractère **null** qui spécifie le nom du port de communication associé à la ligne, à l’adresse ou à l’appel.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-113">The **szDeviceName** member is a **null**-terminated string that specifies the name of the communications port associated with the line, address, or call.</span></span>

<span data-ttu-id="e4fa8-114">Si **hComm** est un handle valide, vous pouvez l’utiliser dans des appels ultérieurs à des fonctions de fichier, telles que [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), pour envoyer et recevoir des données sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-114">If **hComm** is a valid handle, you can use it in subsequent calls to file functions, such as [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), to send and receive data on the call.</span></span> <span data-ttu-id="e4fa8-115">Lorsque vous avez terminé d’utiliser le port de communication et, de préférence, avant d’utiliser la fonction [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) pour libérer l’appel, vous devez fermer le port à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="e4fa8-115">When you are finished using the communications port and preferably before you use the [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) function to deallocate the call, you must close the port by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="e4fa8-116">Lorsque vous utilisez les fonctions [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) et [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) , certains fournisseurs de services requièrent que les données de configuration pour cette classe d’appareil aient le format suivant :</span><span class="sxs-lookup"><span data-stu-id="e4fa8-116">When using the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions, some service providers require that the configuration data for this device class have the following format:</span></span>

``` syntax
typedef struct  tagDEVCFG  {
  DEVCFGHDR   dfgHdr;
  COMMCONFIG  commconfig;
} DEVCFG, *PDEVCFG, FAR* LPDEVCFG;

// Device setting information
typedef struct  tagDEVCFGDR  {
  DWORD       dwSize;
  DWORD       dwVersion;
  WORD        fwOptions;
  WORD        wWaitBong;
} DEVCFGHDR;
```

<span data-ttu-id="e4fa8-117">Voici des informations sur la configuration de l’appareil à utiliser avec les fonctions [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) et [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .</span><span class="sxs-lookup"><span data-stu-id="e4fa8-117">The following is device configuration information for use with the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions.</span></span>

<dl> <dt>

<span data-ttu-id="e4fa8-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="e4fa8-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="e4fa8-119">Somme de la taille de la structure **DEVCFGHDR** et de la taille réelle de la structure [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) .</span><span class="sxs-lookup"><span data-stu-id="e4fa8-119">Sum of the size of the **DEVCFGHDR** structure and the actual size of the [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e4fa8-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="e4fa8-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e4fa8-121">Numéro de version de la structure Unimodem **DevConfig** .</span><span class="sxs-lookup"><span data-stu-id="e4fa8-121">Version number of the Unimodem **DevConfig** structure.</span></span> <span data-ttu-id="e4fa8-122">Ce membre peut être MDMCFG \_ version (0x00010003).</span><span class="sxs-lookup"><span data-stu-id="e4fa8-122">This member can be MDMCFG\_VERSION (0x00010003).</span></span>

</dd> <dt>

<span data-ttu-id="e4fa8-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span><span class="sxs-lookup"><span data-stu-id="e4fa8-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span></span>
</dt> <dd>

<span data-ttu-id="e4fa8-124">Indicateurs d’option qui s’affichent sur la page d’options Unimodem.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-124">Option flags that appear on the Unimodem Option page.</span></span> <span data-ttu-id="e4fa8-125">Ce membre peut être une combinaison de ces valeurs :</span><span class="sxs-lookup"><span data-stu-id="e4fa8-125">This member can be a combination of these values:</span></span>

<dl> <dt>

<span data-ttu-id="e4fa8-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>\_Pré terminal (1)</span><span class="sxs-lookup"><span data-stu-id="e4fa8-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>TERMINAL\_PRE (1)</span></span>
</dt> <dd>

<span data-ttu-id="e4fa8-127">Affiche l’écran pré-terminal.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-127">Displays the pre-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="e4fa8-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>\_Poste de terminal (2)</span><span class="sxs-lookup"><span data-stu-id="e4fa8-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>TERMINAL\_POST (2)</span></span>
</dt> <dd>

<span data-ttu-id="e4fa8-129">Affiche l’écran après le terminal.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-129">Displays the post-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="e4fa8-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>\_Numérotation manuelle (4)</span><span class="sxs-lookup"><span data-stu-id="e4fa8-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>MANUAL\_DIAL (4)</span></span>
</dt> <dd>

<span data-ttu-id="e4fa8-131">Compose le téléphone manuellement, si cela est possible.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-131">Dials the phone manually, if capable of doing so.</span></span>

</dd> <dt>

<span data-ttu-id="e4fa8-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>\_Lumières de lancement (8)</span><span class="sxs-lookup"><span data-stu-id="e4fa8-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>LAUNCH\_LIGHTS (8)</span></span>
</dt> <dd>

<span data-ttu-id="e4fa8-133">Affiche l’icône de modem dans la zone État de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-133">Displays the modem icon in the status area of the taskbar.</span></span>

<span data-ttu-id="e4fa8-134">Seule la valeur des lumières de lancement \_ est définie par défaut</span><span class="sxs-lookup"><span data-stu-id="e4fa8-134">Only the LAUNCH\_LIGHTS value is set by default</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e4fa8-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span><span class="sxs-lookup"><span data-stu-id="e4fa8-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span></span>
</dt> <dd>

<span data-ttu-id="e4fa8-136">Nombre de secondes (en granularité de deux secondes) pour remplacer l’attente de la tonalité ($).</span><span class="sxs-lookup"><span data-stu-id="e4fa8-136">Number of seconds (in two seconds granularity) to replace the wait for credit tone ($).</span></span>

</dd> <dt>

<span data-ttu-id="e4fa8-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span><span class="sxs-lookup"><span data-stu-id="e4fa8-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span></span>
</dt> <dd>

<span data-ttu-id="e4fa8-138">Structure [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) qui peut être utilisée avec les fonctions de configuration des communications et des modems.</span><span class="sxs-lookup"><span data-stu-id="e4fa8-138">[**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure that can be used with the communications and modem configuration functions.</span></span>

</dd> </dl>

 

 
