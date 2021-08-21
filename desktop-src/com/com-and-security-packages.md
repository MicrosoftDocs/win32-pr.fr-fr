---
title: Packages COM et de sécurité
description: Windows prend en charge NTLMSSP (fournisseur de Support de sécurité LAN Manager), le protocole d’authentification Kerberos v5 et le package de sécurité Schannel, qui fournit les protocoles PCT 1,0, ssl 2,0, ssl 3,0 et TLS 1,0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ec80a1ea610725716da3640b6e38b2fd0f3282ce6ce778e632c6a5c8e72c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048717"
---
# <a name="com-and-security-packages"></a>Packages COM et de sécurité

Windows prend en charge NTLMSSP (fournisseur de Support de sécurité LAN Manager), le protocole d’authentification Kerberos v5 et le package de sécurité Schannel, qui fournit les protocoles PCT 1,0, ssl 2,0, ssl 3,0 et TLS 1,0. Le Snego est également pris en charge, qui recherche les packages de sécurité disponibles et sélectionne celui qui convient le mieux.

Le tableau suivant indique les niveaux d’authentification pris en charge par les différents packages de sécurité.



| Authentification serveur/client                                                                                           | Prise en charge des packages de sécurité                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Ni le nom de l’autre.<br/>                                                                      | Aucun<br/>                                                  |
| Le client peut authentifier le serveur, mais pas l’inverse.<br/>                                                 | Schannel<br/>                                              |
| Le client ne peut pas détecter le serveur, mais le serveur peut obtenir l’ID d’utilisateur du client.<br/>                    | NTLMSSP<br/>                                               |
| Authentification mutuelle : le client et le serveur peuvent tous les deux connaître le nom de l’autre, si l’autorisation est accordée.<br/> | NTLMSSP (localement), protocole Kerberos V5 et Schannel<br/> |



 

Pour plus d’informations sur ces packages de sécurité, consultez les rubriques suivantes dans cette section :

-   [NTLMSSP](ntlmssp.md)
-   [Protocole Kerberos V5](kerberos-v5-protocol.md)
-   [Schannel](schannel.md)
-   [Snego](snego.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 





