---
description: Pour un certificat donné, la première étape du décodage de l’objet BLOB de certificat consiste à appeler CertCreateCertificateContext, en lui transmettant un pointeur vers le certificat encodé (BLOB).
ms.assetid: b50530e2-15a0-4215-bf18-300cf67d1611
title: Décodage d’une structure CERT_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8eab5a75c2a5906ac875f925845f83f3c411c12a31aeea4825efd795b78eaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100877"
---
# <a name="decoding-a-cert_info-structure"></a>Décodage d’une \_ structure d’informations de certificat

Pour un certificat donné, la première étape du décodage de l' [*objet BLOB*](../secgloss/b-gly.md) de certificat consiste à appeler [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext), en lui transmettant un pointeur vers le certificat encodé (*BLOB*). Lorsque cette fonction est appelée, elle crée un doublon du certificat encodé, crée une structure de type [**CERT \_ Context**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)et crée une structure de type [**CERT \_ info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info). Comme indiqué dans l’illustration suivante, un [*contexte de certificat*](../secgloss/c-gly.md) comprend l' *objet BLOB* de certificat d’origine, une structure c de type **Certificate \_** Certificate et une structure c de type **CERT \_ info**. L’un des membres de la structure de **\_ contexte** du certificat pointe vers la structure d' **\_ informations** de certificat et l’autre vers l’objet blob de certificat encodé.

![contexte du certificat](images/certcntx.png)

L’objet encodé (membre de données) est toujours fourni comme entrée à la fonction [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) , et la sortie est une structure C qui peut ou non avoir des membres encodés, en fonction de la durée du processus.

Il existe un autre membre qui requiert un décodage et qui est le membre d' **extension** . Bien qu’il ne soit pas encodé au niveau [**des \_ informations de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) , il contient des informations encodées. Pour décoder ces informations, procédez comme indiqué dans l’illustration suivante.

![décodage d’informations](images/xtension.png)

Dans la structure des [**\_ informations de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) , le membre **rgExtension** est un pointeur vers un tableau de structures d' [**\_ extension de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) . Chaque structure d' **\_ extension de certificat** a un membre de **valeur** qui est sous forme encodée et doit être décodé. Le membre **value** est passé à la fonction [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) , puis la sortie de la fonction dépend de la valeur du membre **pszObjId** . Notez que, dans l’illustration, deux structures différentes sont générées, l’une des valeurs de type [**CERT \_ Basic \_ Constraints \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) et l’autre de type informations sur l’ID de clé de l’autorité de [**certification \_ \_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info), en fonction de la valeur de **pszObjId**.

 

 
