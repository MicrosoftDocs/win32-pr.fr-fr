---
description: Cette rubrique répertorie les considérations relatives à l’utilisation de l’API de signature numérique XPS pour ajouter des signatures numériques à un document XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Utilisation de l’API de signature numérique XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864954"
---
# <a name="using-xps-digital-signature-api"></a>Utilisation de l’API de signature numérique XPS

Cette rubrique répertorie les considérations relatives à l’utilisation de l’API de signature numérique XPS pour ajouter des signatures numériques à un document XPS.

L’API de signature numérique XPS permet aux applications de demander aux utilisateurs de signer des documents XPS et de vérifier les signatures détectées dans les documents XPS. L’API de signature numérique XPS peut être appliquée à un document XPS sans le charger dans un modèle d’objet XPS, et elle peut être utilisée sur les flux de documents XPS qui sont sérialisés à partir d’un modèle d’objet XPS.

La section des tâches de programmation de l' [API de signature numérique XPS](#xps-digital-signature-api-programming-tasks) contient des rubriques qui décrivent comment programmer avec l’API de signature numérique XPS. Cette rubrique présente les éléments à prendre en considération pour l’utilisation de l’API de signature numérique XPS lors de l’ajout de la prise en charge des signatures numériques à une application.

-   [Tâches de programmation de l’API de signature numérique XPS](#xps-digital-signature-api-programming-tasks)
-   [Remarques spéciales sur la programmation de l’API de signature numérique XPS](#special-notes-about-xps-digital-signature-api-programming)
    -   [Vérification des signatures numériques dans un document XPS](#verifying-digital-signatures-in-an-xps-document)
    -   [Stratégie de signature des signatures numériques](#digital-signature-signing-policy)
    -   [Incorporation d’une chaîne de certificats](#embedding-a-certificate-chain)
    -   [Utilisation de la \_ structure de contexte du certificat](#using-the-cert\_context-structure)
-   [Rubriques connexes](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a>Tâches de programmation de l’API de signature numérique XPS

Cette section contient des rubriques qui décrivent comment effectuer des tâches de programmation à l’aide de l’API de signature numérique XPS.

-   [Tâches courantes de programmation des signatures numériques](basic-digital-signature-programming-tasks.md)<dl>

[Initialiser le gestionnaire de signatures](initialize-the-signature-manager.md)  
    [Signer un document](sign-a-document.md)  
    [Ajouter une demande de signature à un document XPS](add-a-signature-request-to-a-document.md)  
    [Vérifier les signatures de document](verify-document-signatures.md)  
    </dl>
-   [Tâches de programmation de signature numérique supplémentaires](advanced-digital-signature-programming-tasks.md)<dl>

[Charger un certificat à partir d’un fichier](load-a-certificate-from-a-file.md)  
    [Vérifier qu’un certificat prend en charge une méthode de signature](verify-a-certificate-supports-a-signature-method.md)  
    [Vérifier que le système prend en charge une méthode Digest](verify-a-certificate-supports-a-digest-method.md)  
    [Incorporer des chaînes de certificats dans un document](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a>Remarques spéciales sur la programmation de l’API de signature numérique XPS

Les rubriques suivantes nécessitent une attention particulière lorsque vous utilisez l’API de signature numérique XPS.

-   [Vérification des signatures numériques dans un document XPS](#verifying-digital-signatures-in-an-xps-document)
-   [Stratégie de signature des signatures numériques](#digital-signature-signing-policy)
-   [Incorporation d’une chaîne de certificats](#embedding-a-certificate-chain)
-   [Utilisation de la \_ structure de contexte du certificat](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a>Vérification des signatures numériques dans un document XPS

[**IXpsSignature :: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) vérifie uniquement le contenu signé pour déterminer qu’il n’a pas été modifié depuis sa signature. **IXpsSignature :: Verify** ne vérifie pas les certificats qui ont été utilisés pour signer le contenu du document.

Pour plus d’informations sur les certificats et le chiffrement, consultez [à propos du chiffrement](/windows/desktop/SecCrypto/about-cryptography).

Pour obtenir un exemple de vérification des signatures de document dans un programme, consultez [vérifier les signatures de documents et les certificats](verify-document-signatures.md).

### <a name="digital-signature-signing-policy"></a>Stratégie de signature des signatures numériques

La stratégie de signature de signature numérique détermine les parties d’un document XPS signées. Une option de stratégie de signature consiste à signer les relations de signature qui démarrent à partir de la partie origine de la signature. Étant donné que les relations de signature changent avec chaque signature ajoutée, les signatures qui sont effectuées dans le cadre de cette stratégie s’interrompent lors de l’ajout de nouvelles signatures. Assurez-vous que vous comprenez clairement les implications et les effets de la définition de cette stratégie. dans le cas contraire, un comportement inattendu ou indésirable peut se produire.

Pour plus d’informations sur les stratégies de signature, consultez [**\_ \_ stratégie**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)de signature XPS.

### <a name="embedding-a-certificate-chain"></a>Incorporation d’une chaîne de certificats

Les certificats qui composent la chaîne d’approbation d’un certificat spécifique peuvent être ajoutés à un document XPS. L’incorporation de ces certificats peut faciliter, dans des scénarios hors ligne, qu’une application vérifie les certificats qu’une signature numérique utilise.

Pour plus d’informations sur la façon d’incorporer des certificats dans un document XPS, consultez [incorporer des chaînes de certificats dans un document](embedding-certificate-trust-chains-in-a-document.md).

### <a name="using-the-cert_context-structure"></a>Utilisation de la \_ structure de contexte du certificat

Le [**\_ contexte**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificat et les structures d' [**\_ informations**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) de certificat sont les structures de données principales qui contiennent les informations de certificat. Pour plus d’informations sur l’utilisation de ces structures, consultez [utilisation d’une \_ structure de données d’informations de certificat](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).

[**Certificat \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Les structures de contexte retournées par les fonctions API de chiffrement doivent être libérées lorsqu’elles ne sont plus nécessaires. Pour libérer une structure de **\_ contexte de certificat** , appelez la fonction [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches courantes de programmation des signatures numériques](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[Tâches de programmation de signature numérique supplémentaires](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[**contexte du certificat \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**\_informations sur le certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**\_stratégie de signature XPS \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
