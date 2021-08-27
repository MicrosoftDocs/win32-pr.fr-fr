---
title: Codes d’erreur LDAP pour ADSI
description: Lorsqu’un serveur LDAP génère une erreur et transmet l’erreur au client, l’erreur est ensuite convertie en chaîne par le client LDAP.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6280784d8bf9fc9c692cb38f1ca2d0e76646b1d2a3d464e516f03e7ac682fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005509"
---
# <a name="ldap-error-codes-for-adsi"></a>Codes d’erreur LDAP pour ADSI

Lorsqu’un serveur LDAP génère une erreur et transmet l’erreur au client, l’erreur est ensuite convertie en chaîne par le client LDAP.

Cette méthode est similaire aux [codes d’erreur Win32 pour ADSI](win32-error-codes-for-adsi.md). Dans cet exemple, le code d’erreur du client est l’erreur WIN32 0x80072020.

**Pour déterminer les codes d’erreur LDAP pour ADSI**

1.  Supprimez 8007 du code d’erreur WIN32. Dans l’exemple, la valeur hexadécimale restante est 2020.
2.  Convertit la valeur hexadécimale restante en valeur décimale. Dans l’exemple, la valeur hexadécimale restante 2020 est convertie en valeur décimale 8224.
3.  Dans le fichier WinError. h, recherchez la définition de la valeur décimale. Dans l’exemple, 8224L correspond à l’erreur erreur erreurs du **\_ service d’annuaire \_ \_**.
4.  Remplacez le préfixe **Error \_ DS** par **LDAP \_**. Dans l’exemple, la nouvelle définition est **\_ \_ erreur LDAP Operations**.
5.  Dans le fichier Winldap. h, recherchez la valeur de la définition de l’erreur LDAP. Dans l’exemple, la valeur de **l' \_ \_ erreur opérations LDAP** dans le fichier Winldap. h est 0x01.

 

 




