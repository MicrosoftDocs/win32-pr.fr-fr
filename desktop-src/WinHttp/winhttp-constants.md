---
description: Cette rubrique identifie les constantes utilisées par WinHTTP.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Constantes WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7c277b4235e23254000766fdef53d25f19ddbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484985"
---
# <a name="winhttp-constants"></a>Constantes WinHTTP

WinHTTP utilise les constantes suivantes :

<dl> <dt>

[**Messages d’erreur**](error-messages.md)
</dt> <dd>

Messages d’erreur spécifiques aux fonctions WinHTTP. Ces fonctions retournent également des messages d’erreur Windows, le cas échéant. La valeur qui correspond à chaque constante est la valeur de la constante pour les fonctions d’interface de programmation d’applications (API) et les 16 bits inférieurs du numéro d’erreur pour l’objet [**WinHttpRequest**](winhttprequest.md) .

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

</dd> <dt>

[**Indicateurs d’informations de requête**](query-info-flags.md)
</dt> <dd>

Attributs et modificateurs utilisés par [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).

</dd> </dl>

 

 



