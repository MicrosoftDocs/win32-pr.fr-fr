---
description: Utilisé avec le fournisseur DSS (Digital Signature standard) pour exporter les clés et importer les clés dans, le fournisseur de services de chiffrement (CSP).
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: Objets BLOB de clé du fournisseur DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951086"
---
# <a name="dss-provider-key-blobs"></a>Objets BLOB de clé du fournisseur DSS

Les [*objets BLOB*](../secgloss/b-gly.md) sont utilisés avec le fournisseur DSS ( [*Digital Signature standard*](../secgloss/d-gly.md) ) pour exporter les clés et importer les clés dans, le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).

-   [Objets BLOB de clé publique](#public-key-blobs)
-   [Objets BLOB de clé privée](#private-key-blobs)

## <a name="public-key-blobs"></a>Objets BLOB de clé publique

Une [*clé publique*](../secgloss/p-gly.md) DSS est exportée et importée en tant qu’objet BLOB, une séquence d’octets structurée comme suit.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

Le tableau suivant décrit ces composants. Toutes les valeurs sont au format [*Little endian*](../secgloss/l-gly.md) .



| Champ          | Description                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Structure [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) . Le membre **magique** doit avoir la valeur 0x31535344. Ce nombre hexadécimal est l’encodage [*ASCII*](../secgloss/a-gly.md) de DSS1. |
| g              | Séquence d' **octets** . Générateur, g. Doit avoir la même longueur que p. S’il n’est pas de la même longueur que p, il doit être rempli avec 0x00 octets.                                                                      |
| p              | Séquence d' **octets** . Le modulo principal, p. Le bit le plus significatif de l’octet le plus significatif doit être défini sur un.                                                                                                 |
| publickeystruc | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                |
| q              | Séquence d' **octets** . La longueur prime, q, 20 octets. Le bit le plus significatif de l’octet le plus significatif doit être défini sur un.                                                                                     |
| seedstruct     | Structure [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) . Valeurs de départ et de compteur pour la vérification des premiers.                                                                                                                                |
| y              | Séquence d' **octets** . Clé publique, y. Doit avoir la même longueur que p. S’il n’est pas de la même longueur que p, il doit être rempli avec 0x00 octets.                                                                         |



 

> [!Note]  
> Les [*objets BLOB de clé publique*](../secgloss/p-gly.md) ne sont pas chiffrés. Elles contiennent des clés publiques sous forme de [*texte en clair*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>Objets BLOB de clé privée

Une [*clé privée*](../secgloss/p-gly.md) DSS est exportée et importée sous la forme d’une séquence d’octets structurée comme suit.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

Le tableau suivant décrit chaque composant. Toutes les valeurs sont au format [*Little endian*](../secgloss/l-gly.md) .



| Champ          | Description                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Structure [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) . Le membre **magique** doit être défini sur 0x32535344. Ce nombre hexadécimal est l’encodage [*ASCII*](../secgloss/a-gly.md) de DSS2. |
| g              | Séquence d' **octets** . Générateur, g. Doit avoir la même longueur que p. S’il n’est pas de la même longueur que p, il doit être rempli avec 0x00 octets.                                                                |
| publickeystruc | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                          |
| p              | Séquence d' **octets** . Le modulo principal, p. Le bit le plus significatif de l’octet le plus significatif doit être défini sur un.                                                                                           |
| q              | Séquence d' **octets** . Le premier, le q. q a une longueur de 20 octets. Le bit le plus significatif de l’octet le plus significatif doit être défini sur un.                                                                          |
| seedstruct     | Structure [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) . Valeurs de départ et de compteur pour la vérification des premiers.                                                                                                                          |
| x              | Séquence d' **octets** . Exposant secret, x. Doit toujours avoir une longueur de 20 octets. Si x a une longueur inférieure à 20 octets, elle doit être remplie avec 0x00.                                                     |



 

Lors de l’appel de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), le développeur peut choisir de chiffrer ou non la clé. Le **PRIVATEKEYBLOB** est chiffré si le paramètre *hExpKey* contient un handle valide pour une clé de session. Tout sauf la partie [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) de l’objet blob est chiffré.

> [!Note]  
> Les paramètres d’algorithme de chiffrement et de clé de chiffrement ne sont pas stockés avec l’objet BLOB de clé privée. L’application doit gérer et stocker ces informations. Si la valeur zéro est passée pour *hExpKey*, la clé privée est exportée sans chiffrement.

 

> [!Caution]  
> Il est dangereux d’exporter les clés privées sans chiffrement, car elles sont ensuite vulnérables à l’interception et à l’utilisation par des entités non autorisées.

 

 

 
