---
description: Détermine si une adresse IP se trouve dans un sous-réseau spécifique.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: isInNetEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536405"
---
# <a name="isinnetex-function"></a>isInNetEx fonction)

Détermine si une adresse IP se trouve dans un sous-réseau spécifique.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*IPaddress* 
</dt> <dd>

Chaîne contenant des adresses IPv6/IPv4.

</dd> <dt>

*IPprefix* 
</dt> <dd>

Chaîne contenant le préfixe IP délimité par des points-virgules avec les n premiers bits spécifiés dans le champ de bits (par exemple, 3FFE : 8311 : FFFF ::/48 ou 123.112.0.0/16).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

TRUE si l’hôte se trouve dans le même sous-réseau ; Sinon, FALSe.

Retourne également FALSe si le préfixe n’est pas au format approprié ou si des adresses et des préfixes de différents types sont utilisés dans la comparaison (par exemple, préfixe IPv4 et une adresse IPv6).

## <a name="examples"></a>Exemples

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Définitions d’API d’assistance du proxy compatibles IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensions IPv6 du format de fichier de configuration automatique du navigateur](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



