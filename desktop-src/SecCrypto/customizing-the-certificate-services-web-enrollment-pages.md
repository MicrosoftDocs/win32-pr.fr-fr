---
description: Les services de certificats fournissent des pages d’inscription par le Web qui peuvent être utilisées pour demander des certificats.
ms.assetid: 1e198bc8-c712-4d0f-9e3a-35a295445acf
title: Personnalisation des pages d’inscription par le Web des services de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0132ce4e5e1fef588ffc429597717433dd1b780d2f7f35f9c886f1978b5b318a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767794"
---
# <a name="customizing-certificate-services-web-enrollment-pages"></a>Personnalisation des pages d’inscription par le Web des services de certificats

Les [*services de certificats*](../secgloss/c-gly.md) fournissent des pages d’inscription par le Web qui peuvent être utilisées pour demander des certificats. Un administrateur peut personnaliser certains des éléments qui peuvent être affichés dans les pages d’inscription par le Web. Toutefois, vous devez être familiarisé avec les pages d’inscription par le Web et les scripts Web avant d’apporter des modifications. Pour plus d’informations sur les scripts Web, consultez [Scripting](/previous-versions/ms950396(v=msdn.10)).

Les valeurs par défaut des champs nom unique pour organisation, unité d’organisation, localité, État et pays/région correspondent aux valeurs spécifiées pour l' [*autorité de certification*](../secgloss/c-gly.md) (ca) lors de l’installation des services de certificats. Ces valeurs par défaut apparaissent dans les pages Web et peuvent être modifiées par l’utilisateur pendant le processus d’inscription de certificats. Toutefois, si vous souhaitez que d’autres valeurs par défaut apparaissent dans les pages Web, vous pouvez modifier le fichier Certdat. Inc (dans le chemin d’accès \\ *WindowsDirectory* \\ system32 \\ certsrv \\ ); plus précisément, vous pouvez assigner des valeurs personnalisées aux variables suivantes fournies pour la personnalisation.



| Variable            | Description                                                                                                                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sDefaultCompany     | Société par défaut (apparaît dans la [*demande de certificat*](../secgloss/c-gly.md) en tant que champ d’organisation [*X. 509*](../secgloss/x-gly.md) ). |
| sDefaultOrgUnit     | Service par défaut (apparaît dans la demande de certificat en tant que champ d’unité d’organisation X. 509).                                                                                                                                           |
| sDefaultLocality    | Ville par défaut (apparaît dans la demande de certificat en tant que champ d’emplacement X. 509).                                                                                                                                                            |
| sDefaultState       | État/province par défaut (apparaît dans la demande de certificat en tant que champ d’État X. 509).                                                                                                                                                     |
| sDefaultCountry     | Pays/région par défaut (apparaît dans la demande de certificat comme le champ pays/région X. 509).                                                                                                                                            |
| nPendingTimeoutDays | Nombre de jours pendant lesquels l’utilisateur peut récupérer un certificat en attente une fois qu’il a été demandé.                                                                                                                                          |



 

Aucune autre variable ne doit être modifiée dans le fichier Certdat. Inc.

L’exemple suivant définit l’unité d’organisation par défaut sur « marketing ».


```VB
sDefaultOrgUnit="Marketing"
```



En outre, vous pouvez modifier le fichier Certrqtp. Inc pour ajouter, modifier ou supprimer des [*modèles de certificat*](../secgloss/c-gly.md) ou des types disponibles pour l’utilisateur. Ces modèles et types, ainsi que les informations connexes, sont contenus dans un tableau dimensionné appelé rgAvailReqTypes (*m*, 5).

ce tableau, comme tous les tableaux Visual Basic scripting Edition, est basé sur zéro et, par conséquent, la première dimension du tableau, *m*, alloue de la mémoire pour les éléments *m*+ 1. Par conséquent, si vous personnalisez les pages Web dans, vous devez modifier le nombre d’éléments dans le tableau rgAvailReqTypes, définir la dimension *m* sur une valeur inférieure au nombre total d’éléments dont vous avez besoin. Par exemple, si vous avez sept modèles de certificat, modifiez la déclaration de rgAvailReqTypes comme indiqué dans l’exemple suivant.


```VB
Dim rgAvailReqTypes(6,5)
```



La deuxième dimension du tableau, qui a toujours la valeur 5, alloue les six champs qui composent chaque élément. Ces six champs représentent le type ou le modèle de certificat, le nom complet associé à ce modèle ou type, et si le modèle requiert des extensions S/MIME ( [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) ).

Pour faciliter la compréhension de l’accès à ces champs, Certrqtp. Inc fournit également les constantes suivantes que vous pouvez utiliser lors de la définition des valeurs de champ.



| Constante                              | Description                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **OID du champ \_**                        | (S’applique aux autorités de certification autonomes) Index du premier champ de l’élément ; représente un [*identificateur d’objet*](../secgloss/o-gly.md) (OID) pour un type de certificat.<br/>                                                                                                           |
| **modèle de champ \_**                   | (S’applique aux autorités de certification d’entreprise) Index du premier champ de l’élément ; représente un modèle de certificat.<br/>                                                                                                                                                                                                                           |
| **CHAMP \_ FRIENDLYNAME**               | Index du deuxième champ de l’élément ; représente le nom complet (que l’utilisateur verra lors de l’inscription) de l’élément dans le premier champ.                                                                                                                                                                                               |
| **CHAMP \_ CSPLIST**                    | Indexez le troisième champ de l’élément. Liste des noms de [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) autorisés par le modèle. Chaque nom de la liste est séparé par un point d’interrogation ( ?).                                                    |
| **CHAMP \_ CSPLIST2**                   | Indexez le quatrième champ de l’élément. Liste secondaire de noms de [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) autorisés par le modèle. Chaque nom de la liste est séparé par un point d’interrogation ( ?). Cette liste fournit une valeur par défaut différente. |
| **CHAMP \_ EXportable**                 | Indexez le cinquième champ de l’élément. Indique si le modèle spécifie que la clé doit être exportable. Si ce champ contient la valeur « true », la clé peut être exportée. Si ce champ contient « false », la clé ne peut pas être exportée.                                                                                                        |
| **le champ \_ a besoin de \_ \_ fonctionnalités SMIME** | Cette constante n’est pas prise en charge.                                                                                                                                                                                                                                                                                                      |



 

Par exemple, les expressions suivantes affectent l’OID de 1.3.6.1.5.5.7.3.2 au premier champ de l’élément et affectent « certificat de navigateur Web » au deuxième champ de l’élément (la valeur de tableau de zéro indexe le premier élément).


```VB
rgAvailReqTypes(0, FIELD_OID) = "1.3.6.1.5.5.7.3.2"
rgAvailReqTypes(0, FIELD_FRIENDLYNAME) = "Web Browser Certificate"
```



Le résultat de ces attributions est que l’utilisateur verra le texte du **certificat de navigateur Web** lors de l’inscription, et si l’utilisateur sélectionne le **certificat de navigateur Web**, la [*demande de certificat*](../secgloss/c-gly.md) contiendra l’OID 1.3.6.1.5.5.7.3.2.

Le fichier Certrqtp. Inc contient également des constantes qui sont utilisées pour les noms d’affichage des modèles ou des types de certificats. L’exemple suivant illustre le format.


```VB
' Strings for localization.
Const L_WebBrowserCert_Text="Web Browser Certificate"
Const L_EmailProtectionCert_Text="E-Mail Protection Certificate"
Const L_UserTemplateCert_Text="User Certificate"
```



Ces constantes sont définies dans un bloc dans le fichier Certrqtp. Inc, et ce regroupement facilite l’affectation d’une valeur personnalisée à chacune d’elles. Cela s’avère particulièrement utile lorsque vous localisez les noms complets des versions internationales des pages Web.

Enfin, le fichier Certrqtp. Inc contient une variable qui représente le nombre de modèles ou de types de certificats dans le tableau rgAvailReqTypes. Contrairement à la dimension *m* du tableau, définissez la valeur de la variable nAvailReqTypes sur le nombre réel de modèles de certificats ou de types que votre installation utilisera ; Cette valeur ne doit pas être supérieure à *m*+ 1. Bien qu’elle soit déclarée en haut du fichier Certrqtp. Inc, une valeur est assignée à nAvailReqTypes après le remplissage du tableau rgAvailReqTypes, ce qui permet de voir plus facilement le nombre d’éléments réellement utilisés par le tableau. La valeur nAvailReqTypes est utilisée dans une itération ailleurs dans les pages d’inscription par le Web. il est donc important que cette variable reflète précisément le nombre de modèles de certificat ou de types que vous souhaitez afficher pour l’utilisateur.

Notez que l’ajout simple de [*modèles de certificat*](../secgloss/c-gly.md) et de types au fichier Certrqtp. Inc ne garantit pas que l’utilisateur sera en mesure d’obtenir un certificat avec ces traits ; l’autorité de certification doit être autorisée à émettre un certificat pour le type ou le modèle de certificat spécifié.

Les installations peuvent créer leurs propres applications ou pages Web pour demander et recevoir un certificat. Les objets [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) et [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2) autorisent les programmeurs ou les scripteurs à créer des applications de [*demande de certificat*](../secgloss/c-gly.md) .

Pour demander l’émission d’un certificat sur une [*carte à puce*](../secgloss/s-gly.md), vous pouvez utiliser le contrôle d’inscription de carte à puce. Pour plus d’informations et pour obtenir un exemple de code, consultez [**ISCrdEnr**](iscrdenr.md).

 

 
