---
title: Codes d’erreur LDAP pour ADSI
description: Lorsqu’un serveur LDAP génère une erreur et transmet l’erreur au client, l’erreur est ensuite convertie en chaîne par le client LDAP.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124350"
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

 

 




