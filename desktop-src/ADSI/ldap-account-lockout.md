---
title: Verrouillage de compte (fournisseur LDAP)
description: Lorsque le nombre d’échecs de tentative de connexion est dépassé, le compte d’utilisateur est verrouillé pendant une période spécifiée par l’attribut lockoutDuration.
ms.assetid: bf86f6ac-8209-4306-8736-99ce53c93617
ms.tgt_platform: multiple
keywords:
- Verrouillage de compte (fournisseur LDAP)
- Verrouillage de compte ADSI, fournisseur LDAP
- ADSI Provider ADSI, exemples de gestion des utilisateurs, verrouillage de compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b7a25943debfd08469ce9a28463c88159ded9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106538601"
---
# <a name="account-lockout-ldap-provider"></a>Verrouillage de compte (fournisseur LDAP)

Lorsque le nombre d’échecs de tentative de connexion est dépassé, le compte d’utilisateur est verrouillé pendant une période spécifiée par l’attribut [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) . La propriété [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) semble être la propriété à utiliser pour lire et modifier l’état de verrouillage d’un compte d’utilisateur, mais le fournisseur ADSI LDAP ne prend pas en charge avec précision la propriété **IsAccountLocked** . Pour obtenir et définir des données de verrouillage de compte précises, utilisez le fournisseur Winnt. Pour plus d’informations sur l’utilisation de la propriété **IsAccountLocked** avec le fournisseur WinNT, consultez [verrouillage de compte (fournisseur WinNT)](winnt-account-lockout.md).

 

 