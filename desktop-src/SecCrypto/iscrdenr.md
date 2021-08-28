---
description: Représente le contrôle d’inscription de carte à puce.
ms.assetid: ae872206-81e7-4627-b807-4222f75f8ab6
title: Interface ISCrdEnr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 2471f3acbb483af7e1882102527d392a69e2c7494a929f37718b51a17405c92b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867889"
---
# <a name="iscrdenr-interface"></a>Interface ISCrdEnr

L’interface **ISCrdEnr** représente le contrôle d’inscription de carte à puce. Il intéresse principalement les développeurs qui n’utilisent pas Automation. pour la programmation dans Visual Basic ou un autre langage d’automatisation, consultez l’objet [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) .

## <a name="members"></a>Membres

L’interface **ISCrdEnr** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCrdEnr** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **ISCrdEnr** possède ces méthodes.



| Méthode                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**inscriptions**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))                                         | Demande un certificat pour le compte de l’utilisateur et stocke le [*certificat*](../secgloss/c-gly.md) résultant sur la [*carte à puce*](../secgloss/s-gly.md)de l’utilisateur.<br/>                                                                                                                                                |
| [**enumCAName**](iscrdenr-enumcaname.md)                                 | Énumère les noms des autorités de [*certification*](../secgloss/c-gly.md) (ca) pour un nom de modèle de certificat donné.<br/>                                                                                                                                                                                                       |
| [**enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)             | Énumère les noms de modèles de certificats.<br/>                                                                                                                                                                                                                                                                                                                                                               |
| [**enumCSPName**](iscrdenr-enumcspname.md)                               | Énumère le nom des [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) (CSP) disponibles.<br/>                                                                                                                                                                                                               |
| [**getCACount**](iscrdenr-getcacount.md)                                 | Retourne le nombre d’autorités de certification prêtes à émettre un certificat basé sur le modèle de certificat spécifié.<br/>                                                                                                                                                                                                                                                                                                    |
| [**getCAName**](iscrdenr-getcaname.md)                                   | Récupère le nom de l’autorité de certification spécifiée pour un modèle de certificat donné.<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)             | Récupère le nombre de modèles de certificats.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**getCertTemplateName**](iscrdenr-getcerttemplatename.md)               | Récupère le nom du modèle de certificat.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**getCertTemplateSMIME**](iscrdenr-getcerttemplatesmime.md)             | Déterminez si un modèle de certificat contient l’utilisation de la \_ \_ clé de protection de \_ courrier électronique szOID PKIX \_ . Si l’utilisation de la clé fait partie du modèle de certificat, le modèle de certificat prend en charge les opérations S/MIME ( [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) ).<br/> |
| [**getEnrolledCertificateName**](iscrdenr-getenrolledcertificatename.md) | Récupère le nom du certificat résultant d’un appel antérieur réussi à [**ISCrdEnr :: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)). Cette méthode peut également être utilisée pour afficher le certificat dans une boîte de dialogue.<br/>                                                                                                                                                                                                 |
| [**getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)   | Récupère le nom du sujet à partir du certificat de signature. Cette méthode peut également être utilisée pour afficher le certificat dans une boîte de dialogue. <br/>                                                                                                                                                                                                                                                                       |
| [**getUserName**](iscrdenr-getusername.md)                               | Récupère le nom de l’utilisateur au nom duquel l’inscription de certificat est prévue.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**resetUser**](iscrdenr-resetuser.md)                                   | Efface le nom d’utilisateur du contrôle de carte à puce.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)     | Affiche une boîte de dialogue **Sélectionner un certificat** qui permet de sélectionner un certificat de signature (également appelé certificat de l' *agent d’inscription*).<br/>                                                                                                                                                                                                                                                           |
| [**selectUserName**](iscrdenr-selectusername.md)                         | Affiche une boîte de dialogue **Sélectionner un utilisateur** , qui permet de sélectionner un nom d’utilisateur. Le nom d’utilisateur s’applique à l’utilisateur au nom duquel l’inscription de certificat est prévue.<br/>                                                                                                                                                                                                                                     |
| [**setCAName**](iscrdenr-setcaname.md)                                   | Spécifie le nom de l’autorité de certification.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**setCertTemplateName**](iscrdenr-setcerttemplatename.md)               | Spécifie le nom du modèle de certificat.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**setSigningCertificate**](iscrdenr-setsigningcertificate.md)           | Spécifie un certificat de signature (également connu sous le nom de certificat de l' *agent d’inscription*).<br/>                                                                                                                                                                                                                                                                                                                      |
| [**setUserName**](iscrdenr-setusername.md)                               | Spécifie le nom de l’utilisateur au nom duquel l’inscription de certificat est prévue.<br/>                                                                                                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propriétés

L’interface **ISCrdEnr** possède les propriétés suivantes.



| Propriété                                         | Type d’accès           | Description                                                          |
|:-------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**CSPCount**](iscrdenr-cspcount.md)<br/> | Lecture seule<br/>  | Spécifie le nombre de fournisseurs de services de chiffrement. Cette propriété est en lecture seule.<br/> |
| [**CSPName**](iscrdenr-cspname.md)<br/>   | Lecture/écriture<br/> | Nom du fournisseur de services de chiffrement. Cette propriété est en lecture/écriture. <br/>        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



 

 
