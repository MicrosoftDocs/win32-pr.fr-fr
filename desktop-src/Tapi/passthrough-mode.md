---
description: Lorsqu’un appel est actif dans LINEBEARERMODE \_ passthrough, le fournisseur de services offre un accès direct au matériel attaché pour le contrôle par l’application.
ms.assetid: 75e31241-c782-4d50-9590-cf68c0505add
title: Mode passthrough
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69480fb05b0a86c783b983dcf43f5e241dff865ea6bea16ad4a3744ad06a1fb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959719"
---
# <a name="passthrough-mode"></a>Mode passthrough

Lorsqu’un appel est actif dans **LINEBEARERMODE \_ passthrough**, le fournisseur de services offre un accès direct au matériel attaché pour le contrôle par l’application. Les applications peuvent utiliser ce mode pour le contrôle direct temporaire sur les modems asynchrones, accessibles par le biais des [fonctions de communication](/windows/desktop/DevIO/communications-functions), afin de configurer ou d’utiliser des fonctionnalités spéciales non prises en charge par le fournisseur de services, telles que les télécopies (classe 1, 2, etc.). Ce mode de support est pris en charge par le fournisseur de services Universal Modem Driver (Unimodem).

Les fournisseurs de services qui prennent en charge **LINEBEARERMODE \_ passthrough** l’indiquent dans le membre **DwBearerModes** de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) . Quand **LINEBEARERMODE \_ passthrough** est indiqué, le fournisseur de services Unimodem inclut également dans la zone **DevSpecific** de la structure **LINEDEVCAPS** la clé de Registre utilisée pour accéder aux données relatives au modem associé au périphérique de ligne, au format suivant :

``` syntax
struct {
    DWORD dwContents;   // Set to 1 (indicates containing key).
    DWORD dwKeyOffset;  // Offset to key from start of this
                        // structure (not from start of
                        // LINEDEVCAPS structure).
                        // 8 in this case. 
    BYTE rgby[...];     // Place that contains null-terminated
                        // registry key. 
}
```

Par exemple :

``` syntax
    00000001 00000008 74737953 435c6d65  ........System\C
    65727275 6f43746e 6f72746e 7465536c  urrentControlSet
    7265535c 65636976 6c435c73 5c737361  urrentControlSet
    65646f4d 30305c6d xx003030 xxxxxxxx  Modem\0000.
```

Cette clé de Registre peut ensuite être ouverte à l’aide de la fonction [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) .

Le mode passthrough est appelé le plus souvent à l’aide de la fonction [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , en définissant le bit **LINEBEARERMODE \_ passthrough** dans le membre **dwBearerMode** de la structure [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) vers laquelle pointe le paramètre *lpCallParams* . Une fois cette opération effectuée, le fournisseur de services ouvre le port série sur le modem et place immédiatement l’appel dans **LINECALLSTATE \_ connecté**. L’application peut ensuite utiliser la fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) avec la classe d’appareil « comm/datamodem » pour obtenir un descripteur de fichier ouvert en lecture et en écriture sur le port comm.

Le mode passthrough peut être appelé en réponse à un appel entrant. En règle générale, les applications appellent le mode passthrough pendant que l’appel se trouve dans l' **\_ offre LINECALLSTATE**, avant que l’appel ne soit répondu. Au lieu d’appeler [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer), l’application appelle [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams), en transmettant **LINEBEARERMODE \_ passthrough** en tant que paramètre *dwBearerMode* . Lorsque cela est fait, comme avec [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), l’appel est immédiatement placé dans **LINECALLSTATE \_ connecté** par le fournisseur de services, et l’application peut obtenir un handle vers le port ouvert à l’aide de [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid). La fonction **lineSetCallParams** peut être appelée lorsque l’appel est dans **l' \_ offre LINECALLSTATE**, **LINECALLSTATE \_ accepté** ou **LINECALLSTATE \_ connecté**.

Le mode passthrough se termine normalement en appelant [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) sur le descripteur d’appel obtenu à partir de [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) ou la première [**ligne \_ CALLSTATE**](line-callstate.md) message, si l’appel était un appel entrant. Le fournisseur de services ferme le port et restaure le modem à son état par défaut. L’application doit appeler [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) sur le handle qu’elle a reçu de [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).

Le mode passthrough peut également être arrêté en appelant [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) avec le paramètre *DwBearerMode* défini sur **LINEBEARERMODE \_ Voice**. Le type de support (mode) défini par [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode) est supposé être en vigueur. Si **LINEMEDIAMODE \_ DATAMODEM** est actif, le fournisseur de services prend l’appel comme s’il s’agissait d’un appel de modem de données déjà en cours ; si [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) est appelé par la suite, le fournisseur de services émet les commandes de modem appropriées ou les modifications de l’état de l’interface pour supprimer un appel de données.

> [!Note]  
> Si le mode passthrough est terminé alors que l’appel est en cours, le fournisseur de services TAPI (TSP) de la ligne peut restaurer les paramètres de modem à leur état par défaut. Unimodem est un exemple de TSP qui restaure toujours les paramètres du modem lorsqu’il termine le mode passthrough. Pour cette raison, le mode passthrough ne peut pas être utilisé comme méthode pour configurer l’appareil. Le mode passthrough ne doit être utilisé que pour des activités distinctes qui peuvent être considérées comme terminées lorsque l’exécution de passthrough est terminée. Les exemples d’activités qui peuvent utiliser le mode passthrough incluent l’envoi d’une télécopie ou la lecture de données audio/Wave via un protocole de modem propriétaire.

 

 

 
