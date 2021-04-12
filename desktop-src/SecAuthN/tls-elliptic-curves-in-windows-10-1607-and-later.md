---
description: Courbes elliptiques activées dans Windows 10 version 1607 et versions ultérieures.
title: Des courbes elliptiques TLS dans Windows 10 version 1607 et versions ultérieures
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 813a7c117f5f1e3fc1c6484fc57d1c9f14cf9567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209697"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a>Des courbes elliptiques TLS dans Windows 10 version 1607 et versions ultérieures

Pour Windows 10, versions 1607 et ultérieures, les courbes elliptiques suivantes sont activées et, par défaut, dans cet ordre de priorité, utilisez le fournisseur Microsoft Schannel :

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
- Pour utiliser la stratégie de groupe, [configurez l’ordre des courbes ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) sous Configuration ordinateur > modèles d’administration > les paramètres de configuration réseau > SSL avec la liste priorité pour toutes les courbes elliptiques que vous souhaitez activer.

- Pour utiliser PowerShell, consultez [applets](/powershell/module/tls) de commande TLS pour obtenir une liste complète de la syntaxe et des descriptions de l’applet de commande TLS.


> [!NOTE]
> Avant Windows 10, les chaînes de suite de chiffrement étaient ajoutées à la courbe elliptique pour déterminer la priorité de la courbe. Windows 10 prend en charge un paramètre d’ordre de priorité de courbe elliptique, ce qui signifie que le suffixe de courbe elliptique n’est pas obligatoire et est remplacé par le nouvel ordre de priorité de la courbe elliptique, le cas échéant, pour permettre aux organisations d’utiliser la stratégie de groupe pour configurer différentes versions de Windows avec les mêmes suites de chiffrement.


## <a name="see-also"></a>Voir aussi

[Configuration de l’ordre des courbes ECC TLS](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Gestion de l’ordre ECC TLS](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[Gestion des courbes ECC Windows à l’aide de stratégie de groupe](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[Applets de commande TLS](/powershell/module/tls)
