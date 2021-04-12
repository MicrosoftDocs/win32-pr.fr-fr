---
description: Les services de certificats prennent en charge le renouvellement d’une autorité de certification.
ms.assetid: b6c76642-9a23-471e-af08-58e91d778f09
title: Renouvellement de l’autorité de certification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de57cd16ae6fc4c90bfeea411a06efcb14d028b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951458"
---
# <a name="certification-authority-renewal"></a>Renouvellement de l’autorité de certification

Les [*services de certificats*](../secgloss/c-gly.md) prennent en charge le renouvellement d’une autorité de [*certification*](../secgloss/c-gly.md) . Le renouvellement est l’émission d’un nouveau certificat permettant à l’autorité de certification d’étendre la durée de vie de l’autorité de certification au-delà de la date de fin de son certificat d’origine. Vous pouvez renouveler une autorité de certification en tant que tâche dans le composant logiciel enfichable MMC Autorité de certification ou à l’aide de l’outil Certutil.exe (avec la commande **-renewCert** ).

Chaque renouvellement aboutit à un nouveau certificat d’autorité de certification. Toutefois, l’administrateur peut soit générer une nouvelle paire de clés publique/privée, soit réutiliser la paire de clés publique/privée existante pour le certificat de l’autorité de certification. Pour la cohérence et l’intégrité, les certificats d’autorité de certification et les [*listes de révocation de certificats*](../secgloss/c-gly.md) émis par l’autorité de certification avant son renouvellement seront disponibles une fois que l’autorité de certification a été renouvelée. Pour les rendre disponibles, les services de certificats maintiennent un index des certificats, des listes de révocation de certificats et des clés de l’autorité de certification.

Les index et les noms de suffixes des certificats d’autorité de certification et des listes de révocation de certificats au cours des différentes opérations de renouvellement de l’autorité de certification



| Opération                | Index du certificat d’autorité de certification | Suffixe du nom de fichier du certificat d’autorité de certification | Liste de révocation de certificats et index de clé | Suffixe de liste de révocation de certificats et de conteneur de clé |
|--------------------------|----------------------|---------------------------------|-------------------|-----------------------------------|
| Installation d’origine de l’autorité de certification | 0                    | ""                              | 0                 | ""                                |
| Renouvellement avec une nouvelle clé     | 1                    | « (1) »                           | 1                 | « (1) »                             |
| Renouvellement de réutilisation de la clé      | 2                    | « (2) »                           | 1                 | « (1) »                             |
| Renouvellement de réutilisation de la clé      | 3                    | « (3) »                           | 1                 | « (1) »                             |
| Renouvellement avec une nouvelle clé     | 4                    | « (4) »                           | 4                 | « (4) »                             |
| Renouvellement de réutilisation de la clé      | 5                    | « (5) »                           | 4                 | « (4) »                             |
| Renouvellement avec une nouvelle clé     | 6                    | « (6) »                           | 6                 | « (6) »                             |
| Renouvellement de réutilisation de la clé      | 7                    | « (7) »                           | 6                 | « (6) »                             |



 

Lorsqu’une autorité de certification est installée, l’index du certificat est égal à zéro et le suffixe du certificat est «» (une chaîne vide). Chaque fois que le certificat est renouvelé (que des clés soient réutilisées ou non), l’index du certificat est incrémenté d’une unité et le suffixe du nom du fichier de certificat devient une chaîne au format "(*n*)", où *n* représente le nombre de fois où le certificat de l’autorité de certification a été renouvelé. Après le premier renouvellement, l’index de certificat est 1 et le suffixe de nom de fichier de certificat est « (1) ». Après le deuxième renouvellement, l’index de certificat est 2 et le suffixe de nom de fichier de certificat est « (2) », et ainsi de suite.

Bien que l’index et le suffixe du certificat d’autorité de certification soient incrémentés d’une unité chaque fois que l’autorité de certification est renouvelée, les index de la liste de révocation des certificats et des clés et les suffixes de nom de fichier sont définis sur l’index du certificat d’autorité de certification uniquement si le processus de renouvellement comprend une nouvelle paire de clés publique Si ce n’est pas le cas, les valeurs de ces index et suffixes restent les mêmes que pour le dernier index. Lors du renouvellement, un administrateur spécifie si une nouvelle paire de clés est générée ou si la paire de clés existante est utilisée. (Dans le composant logiciel enfichable MMC Autorité de certification, une option dans l’interface utilisateur spécifie une paire de clés nouvelle ou existante ; dans l’outil Certutil.exe, la commande **certutil-renewCert** renouvelle l’autorité de certification avec une nouvelle paire de clés, tandis que la commande **certutil-renewCert ReuseKeys** renouvelle l’autorité de certification avec la paire de clés existante.)

L’index de la liste de révocation des certificats est directement lié à l’index de clé, qui est défini sur l’index du certificat d’autorité de certification uniquement lorsqu’une nouvelle paire de clés est utilisée pour le renouvellement. Après le premier renouvellement (qui utilisait une nouvelle paire de clés), l’index de la liste de révocation de certificats et de la clé a la valeur 1, et le suffixe de la liste de révocation de certificats et du nom du conteneur de clé est « (1) ». Toutefois, après le deuxième renouvellement, l’index de la liste de révocation de certificats et de la clé reste 1, et le suffixe de liste de révocation de certificats et de nom de conteneur de clé reste également « (1) ». Cela est dû au fait que le deuxième renouvellement a utilisé la paire de clés existante et qu’une seule liste de révocation de certificats est émise pour chaque paire de clés d’autorité de certification.

Vous pouvez récupérer les certificats et les listes de révocation de certificats d’autorité de certification indexés en appelant la méthode **GetCertificateProperty** (dans les interfaces [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) et [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) ). Lorsque vous récupérez certaines propriétés associées au certificat ou à la liste de révocation des certificats de l’autorité de certification, vous pouvez ajouter l’index de base zéro du certificat de l’autorité de certification aux noms des propriétés. Par exemple, pour récupérer l’index de la liste de révocation de certificats qui correspond au troisième certificat de l’autorité de certification, transmettez la propriété « CRLIndex. 2 » à [**ICertServerPolicy :: GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty); pour la table, la valeur de la propriété « CRLIndex. 2 » extraite est 1. Une propriété appelée « CertCount » peut être utilisée pour déterminer le nombre de fois que l’autorité de certification a émis un certificat d’autorité de certification.

Les certificats et les listes de révocation de certificats d’autorité de certification contiennent une extension qui fournit des informations sur le certificat et l’index de clé. L’extension est définie dans wincrypt. h comme szOID \_ CERTSRV \_ ca \_ version avec la valeur « 1.3.6.1.4.1.311.21.1 ». Les données d’extension sont une valeur **DWORD** (encodée en tant qu' \_ entier x509 dans l’extension); les 16 bits de poids faible sont l’index de certificat et les 16 bits de poids fort sont l’index de clé.

L’installation initiale d’une autorité de certification produit un index de certificat de zéro et un index de clé de zéro. Le renouvellement d’un certificat d’autorité de certification entraîne l’incrémentation de l’index de certificat. Si la clé est réutilisée dans le renouvellement, l’index de clé est identique à l’index de clé précédent. Si la clé n’est pas réutilisée, l’index de clé correspondra au nouvel index de certificat.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> </dl>

 

 
