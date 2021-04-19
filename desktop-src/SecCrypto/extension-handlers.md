---
description: À partir de la version 3 du format de certificat X. 509, un certificat peut contenir des extensions de certificat.
ms.assetid: fb106cab-8a61-4a83-8fb4-7c045d905575
title: Gestionnaires d’extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfcf1b47fcc97b87f5956f4584aee07acce04222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536866"
---
# <a name="extension-handlers"></a>Gestionnaires d’extensions

À partir de la version 3 du format de certificat [*X. 509*](../secgloss/x-gly.md) , un certificat peut contenir des extensions de certificat. (Pour obtenir le contenu d’un certificat X. 509, consultez [Propriétés du certificat](certificate-properties.md).) Ces extensions indiquent des informations supplémentaires. Par exemple, une extension peut indiquer des informations d’identification de sujet supplémentaires, ou elle peut indiquer des informations sur l’utilisation de la clé, qui spécifie les tâches (telles que la signature ou le chiffrement) pour lesquelles une clé peut être utilisée. Un ensemble d’extensions standard est défini pour l’utilisation de l’application, et les extensions peuvent également être personnalisées.

Chaque extension est associée à une chaîne d’identificateur d’objet qui identifie le type d’informations supplémentaires et une structure de données qui contient ces informations. Par exemple, l’identificateur d’objet de l’utilisation de la clé est « 2.5.29.15 », ce qui indique des informations sur l’utilisation de la clé. Sa structure de données associée est [**un \_ \_ objet BLOB**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_bit_blob) de chiffrement (champ de bits) spécifiant comment la clé peut être utilisée.

Une extension peut être ajoutée à un certificat avant son émission. Lorsque le certificat est émis, toutes les extensions activées font partie du certificat. Si une extension est marquée comme critique, son utilisation doit être connue de l’application using, et l’application doit adhérer à l’intention ou à la valeur de l’extension. Les services de certificats autorisent la définition d’extensions sur un certificat non émis par le biais des méthodes fournies par [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) et [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy). Pour plus d’informations sur les extensions de certificat, consultez Certificate [**\_ extension**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) dans la documentation CryptoAPI. Pour plus d’informations sur les structures de données d’extension de certificat courantes, consultez [structures d’extension de certificat X. 509](cryptography-structures.md).

Le gestionnaire d’extensions est un objet COM qui fournit des routines pour l’encodage des extensions et des types de données plus complexes, mais couramment utilisés, tels que IA5String ou PrintableString.

Les extensions qui ont les types de données **Date**, **long** et **BSTR** ne nécessitent pas de gestionnaire d’extensions. Le module de stratégie appelle simplement [**ICertServerPolicy :: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) avec le paramètre de *type* défini sur une valeur représentant le type de données d’extension : PROPTYPE \_ date, PROPTYPE \_ long ou PROPTYPE \_ String. Il passe ensuite l’extension au moteur du serveur. Le moteur serveur, à son tour, exécute l’encodage ASN. 1 ( [*Abstract Syntax Notation One*](../secgloss/a-gly.md) ) avant de stocker l’extension dans le certificat.

Toutefois, les extensions qui ont des types de données autres que ces types par défaut doivent être codées ASN. 1 par un gestionnaire d’extension avant que le module de stratégie les transmette au moteur du serveur. Lorsque le module de stratégie appelle [**ICertServerPolicy :: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) pour transmettre une extension ASN. 1 au moteur du serveur, il doit définir le paramètre de *type* sur PROPTYPE \_ Binary. Le moteur de serveur stocke ensuite simplement cette extension encodée dans le certificat.

Le gestionnaire d’extensions par défaut, Certenc.dll, exporte plusieurs interfaces **ICertEncodeXXX** et peut être appelé par le module de stratégie. Les informations de type nécessaires sont également contenues dans Certencl.dll qui est fourni dans le kit de développement logiciel (SDK) de la plateforme. Chaque interface fournit une méthode **encode** qui retourne une extension de certificat encodée ASN. 1 au module de stratégie dans un format binaire. Le module de stratégie peut ensuite définir l’extension dans un certificat en appelant la méthode [**ICertServerPolicy :: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) .

Pour plus d’informations, consultez [écriture de gestionnaires d’extensions personnalisés](writing-custom-extension-handlers.md).

 

 
