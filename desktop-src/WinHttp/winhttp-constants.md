---
description: Cette rubrique identifie les constantes utilisées par WinHTTP.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Constantes WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e37b0e4de7aa3df5e155933bea2be25386c1637
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013152"
---
# <a name="winhttp-constants"></a>Constantes WinHTTP

WinHTTP utilise les constantes suivantes :

<dl>

<dt>

[**Messages d'erreur**](error-messages.md)
</dt> <dd>

Messages d’erreur spécifiques aux fonctions WinHTTP. ces fonctions retournent également Windows des messages d’erreur, le cas échéant. La valeur qui correspond à chaque constante est la valeur de la constante pour les fonctions d’interface de programmation d’applications (API) et les 16 bits inférieurs du numéro d’erreur pour l’objet [**WinHttpRequest**](winhttprequest.md) .

</dd> <dt>

[**Codes d’état HTTP**](http-status-codes.md)
</dt> <dd>

Les constantes et les valeurs correspondantes qui indiquent les codes d’état HTTP renvoyés par les serveurs sur Internet.

</dd> <dt>

[**Indicateurs d’option**](option-flags.md)
</dt> <dd>

Indicateurs d’option pris en charge par [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) et [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Tous les indicateurs d’option valides ont une valeur supérieure ou égale à la \_ première \_ option WinHTTP et sont inférieures ou égales à la \_ dernière option WinHTTP \_ .

</dd> <dt>

[**\_port Internet**](internet-port.md)
</dt> <dd>

Valeur de mot indiquant le port.

</dd> <dt>

[**\_schéma Internet**](internet-scheme.md)
</dt> <dd>

Schémas Internet pris en charge par WinHTTP.

</dd>

<dt>

[**Indicateurs d’informations de requête**](query-info-flags.md)
</dt>
<dd>

Attributs et modificateurs utilisés par [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).
</dd>

<dt>

**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**
</dt>
<dd>

A la valeur 0x00000001. Indique à [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) que les chaînes passées sont des chaînes Unicode.
</dd>

<dt>

**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**
</dt>
<dd>

A la valeur 0x0000000000000001ull. Ordonne à [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) de ne pas terminer l’appel tant que le tampon de données fourni n’a pas été rempli ou que la réponse n’est pas terminée. Le passage de cet indicateur rend le comportement de **WinHttpReadDataEx** équivalent à celui de [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).
</dd>

</dl>
