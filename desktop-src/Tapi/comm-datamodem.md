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
# <a name="commdatamodem"></a>comm/datamodem

La classe d’appareil comm/datamodem se compose d’appareils datamodem. Vous accédez à ces appareils à l’aide des [fonctions](/windows/desktop/DevIO/communications-functions)de [fichier](/windows/desktop/FileIO/file-management-functions) et de communication. Les appareils de cette classe sont associés à des appareils de ligne qui prennent en charge le \_ type de média LINEMEDIAMODE DATAMODEM, qui est spécifié dans le membre **dwMediaModes** de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour le périphérique de ligne.

La fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) remplit une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en affectant à **dwStringFormat** la \_ valeur binaire STRINGFORMAT et en ajoutant les membres supplémentaires suivants :

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

Le membre **hComm** est le descripteur du port de communication ouvert. Ce membre a la valeur **null** si le port n’est pas encore ouvert ou si le paramètre *dwSelect* de [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) n’est pas la valeur de l' \_ appel LINECALLSELECT. Si un appel est actif, le fournisseur de services ouvre généralement le port lui-même pour contrôler directement le matériel de communication, mais il n’est nécessaire que pour retourner un handle valide si la ligne est connectée. Le fournisseur de services ouvre le port à l’aide de la \_ valeur de chevauchement de l’indicateur \_ de fichier, puis il configure le port à l’aide des paramètres spécifiés par la fonction [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) . Vous pouvez définir des options de configuration supplémentaires pour l’appareil en utilisant des fonctions de communication avec le handle retourné.

Le membre **szDeviceName** est une chaîne se terminant par un caractère **null** qui spécifie le nom du port de communication associé à la ligne, à l’adresse ou à l’appel.

Si **hComm** est un handle valide, vous pouvez l’utiliser dans des appels ultérieurs à des fonctions de fichier, telles que [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), pour envoyer et recevoir des données sur l’appel. Lorsque vous avez terminé d’utiliser le port de communication et, de préférence, avant d’utiliser la fonction [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) pour libérer l’appel, vous devez fermer le port à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

Lorsque vous utilisez les fonctions [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) et [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) , certains fournisseurs de services requièrent que les données de configuration pour cette classe d’appareil aient le format suivant :

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

Voici des informations sur la configuration de l’appareil à utiliser avec les fonctions [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) et [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**
</dt> <dd>

Somme de la taille de la structure **DEVCFGHDR** et de la taille réelle de la structure [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) .

</dd> <dt>

<span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**
</dt> <dd>

Numéro de version de la structure Unimodem **DevConfig** . Ce membre peut être MDMCFG \_ version (0x00010003).

</dd> <dt>

<span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**
</dt> <dd>

Indicateurs d’option qui s’affichent sur la page d’options Unimodem. Ce membre peut être une combinaison de ces valeurs :

<dl> <dt>

<span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>\_Pré terminal (1)
</dt> <dd>

Affiche l’écran pré-terminal.

</dd> <dt>

<span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>\_Poste de terminal (2)
</dt> <dd>

Affiche l’écran après le terminal.

</dd> <dt>

<span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>\_Numérotation manuelle (4)
</dt> <dd>

Compose le téléphone manuellement, si cela est possible.

</dd> <dt>

<span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>\_Lumières de lancement (8)
</dt> <dd>

Affiche l’icône de modem dans la zone État de la barre des tâches.

Seule la valeur des lumières de lancement \_ est définie par défaut

</dd> </dl> </dd> <dt>

<span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**
</dt> <dd>

Nombre de secondes (en granularité de deux secondes) pour remplacer l’attente de la tonalité ($).

</dd> <dt>

<span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**
</dt> <dd>

Structure [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) qui peut être utilisée avec les fonctions de configuration des communications et des modems.

</dd> </dl>

 

 
