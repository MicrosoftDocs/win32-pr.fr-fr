---
description: Chaque propriété de contrôle d’inscription de certificat est en lecture/écriture et a une valeur par défaut initialisée, ainsi qu’un ensemble de valeurs acceptables.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Utilisation des propriétés du contrôle d’inscription de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127417648"
---
# <a name="using-the-certificate-enrollment-control-properties"></a>Utilisation des propriétés du contrôle d’inscription de certificat

Chaque propriété de contrôle d’inscription de certificat est en lecture/écriture et a une valeur par défaut initialisée, ainsi qu’un ensemble de valeurs acceptables. Vous pouvez définir une propriété sur n’importe quelle valeur dans cet ensemble afin de modifier le comportement des méthodes qui utilisent la propriété. Pour obtenir un comportement souhaité, définissez la propriété avant d’appeler la méthode qui utilise la valeur de cette propriété.

Notez, toutefois, qu’après l’appel des méthodes suivantes

-   [**acceptPKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [**acceptFilePKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [**createPKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [**createFilePKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

la réinitialisation des propriétés suivantes est bloquée

-   [**ProviderType**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [**KeySpec**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [**ProviderFlags**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [**ContainerName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [**ProviderName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

à moins que la méthode [**ICEnroll4 :: Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) soit appelée.

Pour plus d’informations sur les propriétés et les méthodes individuelles, consultez les rubriques de référence pour ces propriétés et méthodes dans la [référence de chiffrement](cryptography-reference.md).

Les sections suivantes contiennent des informations spécifiques à la langue pour la définition et la récupération des propriétés du contrôle d’inscription de certificat :

-   [Propriétés du contrôle d’inscription de certificat en C++](certificate-enrollment-control-properties-in-c-.md)

 

 
