---
description: Représente l’extension de contraintes de base d’un certificat.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: Objet BasicConstraints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541677"
---
# <a name="basicconstraints-object"></a>Objet BasicConstraints

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

L’objet **basicConstraints** représente l’extension de contraintes de base d’un certificat.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **basicConstraints** est utilisé pour effectuer les tâches suivantes :

-   Déterminez si l’extension de contraintes de base est présente.
-   Déterminez si l’extension de contraintes de base est marquée comme critique.
-   Déterminez si le certificat est imposé aux autorités de certification.
-   Déterminez si la contrainte de longueur de chemin d’accès est présente et récupérez la valeur de contrainte de longueur du chemin d’accès.

## <a name="members"></a>Membres

L’objet **basicConstraints** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **basicConstraints** a ces propriétés.



| Propriété                                                                                     | Type d’accès          | Description                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCertificateAuthority**](basicconstraints-iscertificateauthority.md)<br/>         | Lecture seule<br/> | Récupère une valeur booléenne qui indique si le certificat est destiné à une [*autorité de certification*](../secgloss/c-gly.md) (ca).<br/> |
| [**IsCritical**](basicconstraints-iscritical.md)<br/>                                 | Lecture seule<br/> | Récupère une valeur booléenne qui indique si l’extension de contrainte de base est marquée comme critique.<br/>                                                                                                     |
| [**IsPathLenConstraintPresent**](basicconstraints-ispathlenconstraintpresent.md)<br/> | Lecture seule<br/> | Récupère une valeur booléenne qui indique si la contrainte de longueur de chemin d’accès du certificat est présente.<br/>                                                                                                   |
| [**IsPresent**](basicconstraints-ispresent.md)<br/>                                   | Lecture seule<br/> | Récupère une valeur booléenne qui indique si l’extension de contraintes de base est présente. Il s’agit de la propriété par défaut.<br/>                                                                              |
| [**PathLenConstraint**](basicconstraints-pathlenconstraint.md)<br/>                   | Lecture seule<br/> | Récupère la valeur de la contrainte de longueur de chemin d’accès.<br/>                                                                                                                                                      |



 

## <a name="remarks"></a>Notes

Impossible de créer l’objet **basicConstraints** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets de chiffrement](cryptography-objects.md)
</dt> </dl>

 

 
