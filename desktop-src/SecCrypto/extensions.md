---
description: Représente une collection d’objets d’extension.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Objet extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533098"
---
# <a name="extensions-object"></a>Objet extensions

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet **Extensions** représente une collection d’objets d' [**extension**](extension.md) . Chaque objet d' [**extension**](extension.md) représente une extension de certificat unique.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **Extensions** est utilisé pour effectuer les tâches suivantes :

-   Récupérez le nombre d’extensions de certificat dans la collection.
-   Récupérez un objet d' [**extension**](extension.md) spécifique de la collection.
-   Itérez au sein de la collection.

## <a name="members"></a>Membres

L’objet **Extensions** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **Extensions** possède ces propriétés.



| Propriété                                           | Type d’accès          | Description                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extensions-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).<br/> |
| [**Saut**](extensions-count.md)<br/>       | Lecture seule<br/> | Récupère le nombre d’objets d' [**extension**](extension.md) dans la collection.<br/>                                                                                                                                    |
| [**Élément**](extensions-item.md)<br/>         | Lecture seule<br/> | Récupère l’objet d' [**extension**](extension.md) qui représente l’extension de certificat indexée de la collection. Il s’agit de la propriété par défaut.<br/>                                                               |



 

## <a name="remarks"></a>Notes

L’objet **Extensions** est retourné par la méthode [**Certificate. extensions**](certificate-extensions.md) .

Impossible de créer l’objet **Extensions** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
