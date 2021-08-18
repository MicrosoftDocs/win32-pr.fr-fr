---
description: Les services de certificats constituent une base pour l’infrastructure à clé publique (PKI) qui fournit les moyens de protéger et d’authentifier les informations.
ms.assetid: c18f46ca-e805-4b33-8014-79dc34c18531
title: Certificats et clés publiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d5f1996549184b8c56388bdb3ae8395eee077bca31b03e074f4dda8568805b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770619"
---
# <a name="certificates-and-public-keys"></a>Certificats et clés publiques

Les services de certificats constituent une base pour l’infrastructure à clé publique (PKI) qui fournit les moyens de protéger et d’authentifier les informations. La relation entre un détenteur de certificat, l’identité du titulaire du certificat et la [*clé publique*](../secgloss/p-gly.md) du détenteur du certificat est une partie critique de l’infrastructure à clé publique. Cette infrastructure est constituée des éléments suivants :

-   [Paire de clés publique/privée](#the-publicprivate-key-pair)
-   [Demande de certificat](#the-certificate-request)
-   [Autorité de certification](#the-certification-authority)
-   [Le certificat](#the-certificate-request)
-   [La liste de révocation de certificats](#the-certificate-revocation-list)
-   [Votre clé publique utilisée pour le chiffrement](#your-public-key-used-for-encryption)
-   [Votre clé publique utilisée pour la vérification de la signature](#your-public-key-used-for-signature-verification)
-   [Rôle des services de certificats Microsoft](#microsoft-certificate-services-role)

## <a name="the-publicprivate-key-pair"></a>Paire de clés publique/privée

L’infrastructure à clé publique requiert l’utilisation de [*paires de clés publiques/privées*](../secgloss/p-gly.md). La mathématique des paires de clés publiques/privées dépasse le cadre de cette documentation, mais il est important de noter la relation fonctionnelle entre une clé publique et une clé privée. Les [*algorithmes de chiffrement*](../secgloss/c-gly.md) PKI utilisent la [*clé publique*](../secgloss/p-gly.md) du récepteur d’un message chiffré pour chiffrer les données, et la [*clé privée*](../secgloss/p-gly.md) associée et seule la clé privée associée pour déchiffrer le message chiffré.

De même, une [*signature numérique*](../secgloss/d-gly.md) du contenu, décrite plus en détail ci-dessous, est créée avec la clé privée du signataire. La clé publique correspondante, disponible pour tout le monde, est utilisée pour vérifier cette signature. Le secret de la clé privée doit être maintenu, car l’infrastructure est séparée après la compromission de la clé privée.

Étant donné suffisamment de temps et de ressources, une paire de clés publique/privée peut être compromise, c’est-à-dire que la clé privée peut être découverte. Plus la clé est longue, plus il est difficile d’utiliser force brute pour découvrir la clé privée. Dans la pratique, des clés suffisamment fortes peuvent être utilisées pour faciliter la détermination de la clé privée en temps utile, ce qui fait de l’infrastructure à clé publique un mécanisme de sécurité viable.

Une clé privée peut être stockée, au format protégé, sur un disque. dans ce cas, elle ne peut être utilisée qu’avec cet ordinateur, sauf si elle est physiquement déplacée vers un autre ordinateur. Une alternative consiste à avoir une clé sur une carte à puce qui peut être utilisée sur un autre ordinateur, à condition qu’elle dispose d’un lecteur de carte à puce et d’un logiciel de prise en charge.

La clé publique, mais pas la clé privée, du sujet d’un certificat numérique est incluse dans le cadre de la [*demande de certificat*](../secgloss/c-gly.md). (Par conséquent, une paire de clés publique/privée doit exister avant d’effectuer la demande de certificat). Cette clé publique devient partie intégrante du certificat émis.

## <a name="the-certificate-request"></a>Demande de certificat

Avant l’émission d’un certificat, une [*demande de certificat*](../secgloss/c-gly.md) doit être générée. Cette demande s’applique à une entité, par exemple, un utilisateur final, un ordinateur ou une application. Pour la discussion, supposons que l’entité est vous-même. Les détails de votre identité sont inclus dans la demande de certificat. Une fois la demande générée, elle est envoyée à une [*autorité de certification*](../secgloss/c-gly.md) (ca). L’autorité de certification utilise ensuite vos informations d’identité pour déterminer si la demande répond aux critères de l’autorité de certification pour l’émission d’un certificat. Si l’autorité de certification approuve la demande, elle émet un certificat, en tant qu’entité nommée dans la demande.

## <a name="the-certification-authority"></a>Autorité de certification

Avant d’émettre votre certificat, l’autorité de certification vérifie votre identité. Lorsque le certificat est émis, votre identité est liée au certificat, qui contient votre clé publique. Votre certificat contient également la signature numérique de l’autorité de certification (qui peut être vérifiée par toute personne qui reçoit votre certificat).

Étant donné que votre certificat contient l’identité de l’autorité de certification émettrice, une partie intéressée qui approuve cette autorité de certification peut étendre cette approbation à votre certificat. L’émission d’un certificat n’établit pas d’approbation, mais transfère l’approbation. Si le consommateur du certificat ne fait pas confiance à l’autorité de certification émettrice, il n’approuve pas (ou au moins) le certificat.

Une chaîne de certificats signés permet également de transférer l’approbation vers d’autres autorités de certification. Cela permet aux tiers qui utilisent différentes autorités de certification de toujours être en mesure de faire confiance aux certificats (à condition qu’il existe une autorité de certification commune dans la chaîne, autrement dit, une autorité de certification approuvée par les deux parties).

## <a name="the-certificate"></a>Le certificat

En plus de votre clé publique et de l’identité de l’autorité de certification émettrice, le certificat émis contient des informations sur les objectifs de votre clé et certificat. En outre, il comprend le chemin d’accès à la liste des certificats révoqués de l’autorité de certification et spécifie la période de validité du certificat (dates de début et de fin).

En supposant que le consommateur du certificat approuve l’autorité de certification émettrice pour votre certificat, le consommateur du certificat doit déterminer si le certificat est toujours valide en comparant les dates de début et de fin du certificat à l’heure actuelle et en vérifiant que votre certificat ne figure pas dans la liste des certificats révoqués de l’autorité de certification.

## <a name="the-certificate-revocation-list"></a>La liste de révocation de certificats

En supposant que le certificat est utilisé dans un laps de temps valide et que le consommateur du certificat approuve l’autorité de certification émettrice, il existe un autre élément que le consommateur du certificat doit vérifier avant d’utiliser le certificat : la [*liste de révocation de certificats*](../secgloss/c-gly.md) (CRL). Le consommateur du certificat vérifie la liste de révocation de certificats de l’autorité de certification (le chemin d’accès qui est inclus en tant qu’extension dans votre certificat) pour s’assurer que votre certificat ne figure pas dans la liste des certificats qui ont été révoqués. Les listes de révocation de certificats existent car il y a des cas où un certificat n’a pas expiré, mais il ne peut plus être approuvé. Périodiquement, l’autorité de certification publie une liste de révocation de certificats mise à jour. Les consommateurs de certificats sont responsables de la comparaison des certificats à la liste de révocation de certificats actuelle avant de considérer le certificat comme digne de confiance.

## <a name="your-public-key-used-for-encryption"></a>Votre clé publique utilisée pour le chiffrement

Si un expéditeur souhaite chiffrer un message avant de l’envoyer à vous, l’expéditeur récupère d’abord votre certificat. Une fois que l’expéditeur a déterminé que l’autorité de certification est approuvée et que votre certificat est valide et n’est pas révoqué, l’expéditeur utilise votre clé publique (Rappelez-vous qu’il fait partie du certificat) avec des algorithmes de chiffrement pour chiffrer le message en [*texte clair*](../secgloss/p-gly.md) en [*texte chiffré*](../secgloss/c-gly.md). Lorsque vous recevez le texte chiffré, vous utilisez votre clé privée pour déchiffrer le texte chiffré.

Si un tiers intercepte le message électronique chiffré, le tiers ne pourra pas le déchiffrer sans avoir accès à votre [*clé privée*](../secgloss/p-gly.md).

Notez que la majeure partie des activités répertoriées ici sont gérées par les logiciels, et non directement par l’utilisateur.

## <a name="your-public-key-used-for-signature-verification"></a>Votre clé publique utilisée pour la vérification de la signature

Une [*signature numérique*](../secgloss/d-gly.md) est utilisée comme confirmation qu’un message n’a pas été modifié et comme confirmation de l’identité de l’expéditeur du message. Cette signature numérique dépend de votre clé privée et du contenu du message. En utilisant le message comme entrée et votre clé privée, les algorithmes de chiffrement créent la signature numérique. Le contenu du message n’est pas modifié par le processus de signature. Un destinataire peut utiliser votre clé publique (après vérification de la validité de votre certificat, de l’autorité de certification émettrice et de l’état de révocation) pour déterminer si la signature correspond au contenu du message et pour déterminer si le message vous a été envoyé.

Si un tiers intercepte le message souhaité, le modifie (même légèrement), le transmet et la signature d’origine au destinataire, le destinataire, lors de l’examen du message et de la signature, est en mesure de déterminer que le message est suspect. De même, si un tiers crée un message et l’envoie avec une signature numérique factice sous le forme qu’il provenait de vous, le destinataire peut utiliser votre clé publique pour déterminer que le message et la signature ne correspondent pas.

La non- [*répudiation*](../secgloss/n-gly.md) est également prise en charge par les signatures numériques. Si l’expéditeur d’un message signé refuse d’envoyer le message, le destinataire peut utiliser la signature pour réfuter cette revendication.

Notez que la majeure partie des activités répertoriées ici sont également gérées par les logiciels, et non directement par l’utilisateur.

## <a name="microsoft-certificate-services-role"></a>Rôle des services de certificats Microsoft

Les services de certificats Microsoft ont le rôle d’émettre des certificats ou de refuser des demandes de certificats, comme indiqué par les modules de stratégie, qui sont chargés de garantir l’identité du demandeur de certificat. Les services de certificats offrent également la possibilité de révoquer un certificat, ainsi que de publier la liste de révocation de certificats. Les services de certificats peuvent également distribuer de manière centralisée (par exemple, à un service d’annuaire) des certificats émis. La possibilité d’émettre, de distribuer, de révoquer et de gérer des certificats, ainsi que la publication des listes de révocation de certificats, fournit les fonctionnalités nécessaires à l’infrastructure à clé publique.

 

 
