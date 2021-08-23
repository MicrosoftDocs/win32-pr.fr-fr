---
description: courbes elliptiques activées dans Windows 10 version 1607 et versions ultérieures.
title: des courbes elliptiques TLS dans Windows 10 version 1607 et versions ultérieures
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 237d0f7a7b4b2a7fecb99a91f21c55349e7d435b221e1b3297afd1ba614cc92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915844"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a>des courbes elliptiques TLS dans Windows 10 version 1607 et versions ultérieures

pour Windows 10, les versions 1607 et ultérieures, les courbes elliptiques suivantes sont activées et, par défaut, dans cet ordre de priorité, utilisez le fournisseur Microsoft Schannel :

| Chaîne de courbe elliptique | Disponible en mode FIPS |
|-------------|--------------|
| curve25519 | Non |
| NistP256 | Oui |
| NistP384 | Oui |


Les courbes elliptiques suivantes sont prises en charge par le fournisseur Microsoft Schannel, mais ne sont pas activées par défaut :

| Chaîne de courbe elliptique | Disponible en mode FIPS |
|-------------|--------------|
| brainpoolP256r1 | Non |
| brainpoolP384r1 | Non |
| brainpoolP512r1 | Non |
| nistP192 | Non |
| nistP224 | Non |
| nistP521 | Oui |
| secP160k1 | Non |
| secP160r1 | Non |
| secP160r2 | Non |
| secP192k1 | Non |
| secP192r1 | Non |
| secP224k1 | Non |
| secP224r1 | Non |
| secP256k1 | Non |
| secP256r1 | Non |
| secP384r1 | Non |
| secP521r1 | Non |



## <a name="enabling-elliptic-curves"></a>Activation des courbes elliptiques

Pour ajouter des courbes elliptiques, vous pouvez soit déployer une stratégie de groupe, soit utiliser les applets de commande TLS :
- pour utiliser la stratégie de groupe, [configurez l’ordre des courbes ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) sous configuration ordinateur > Modèles d’administration > réseau > configuration SSL Paramètres avec la liste des priorités pour toutes les courbes elliptiques que vous souhaitez activer.

- Pour utiliser PowerShell, consultez [applets](/powershell/module/tls) de commande TLS pour obtenir une liste complète de la syntaxe et des descriptions de l’applet de commande TLS.


> [!NOTE]
> avant Windows 10, les chaînes de suite de chiffrement ont été ajoutées à la courbe elliptique pour déterminer la priorité de la courbe. Windows 10 prend en charge un paramètre d’ordre de priorité de courbe elliptique, si bien que le suffixe de courbe elliptique n’est pas obligatoire et est remplacé par le nouvel ordre de priorité de la courbe elliptique, le cas échéant, pour permettre aux organisations d’utiliser la stratégie de groupe pour configurer différentes versions de Windows avec les mêmes suites de chiffrement.


## <a name="see-also"></a>Voir aussi

[Configuration de l’ordre des courbes ECC TLS](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Gestion de l’ordre ECC TLS](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[gestion des courbes ECC Windows à l’aide de stratégie de groupe](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[Applets de commande TLS](/powershell/module/tls)
