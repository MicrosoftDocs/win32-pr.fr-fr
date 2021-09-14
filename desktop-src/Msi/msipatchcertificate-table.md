---
description: Identifie les certificats de signataire possibles utilisés pour signer numériquement les correctifs.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: Table MsiPatchCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01648e792931fd856a1231a5d876c7db843479df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119746"
---
# <a name="msipatchcertificate-table"></a>Table MsiPatchCertificate

La table MsiPatchCertificate identifie les certificats de signataire possibles utilisés pour signer numériquement les correctifs. La table MsiPatchCertificate contient les informations nécessaires pour activer la mise à [jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md) pour une application.

La table MsiPatchCertificate contient les colonnes suivantes :



| Colonne               | Type                         | Clé | Nullable |
|----------------------|------------------------------|-----|----------|
| PatchCertificate     | [Identificateur](identifier.md) | O   | N        |
| DigitalCertificate\_ | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate
</dt> <dd>

Identificateur unique de cette ligne dans la table MsiPatchCertificate.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Une clé externe dans la première colonne de la [table MsiDigitalCertificate](msidigitalcertificate-table.md). La ligne indiquée dans la table MsiDigitalCertificate contient la représentation binaire du certificat du signataire.

</dd> </dl>

## <a name="remarks"></a>Notes

Les correctifs sont toujours évalués par rapport à la table MsiPatchCertificate qui est active au moment de l’application du correctif. Un correctif peut modifier la table MsiPatchCertificate en ajoutant ou en supprimant des entrées. Cela permet à un correctif de modifier l’évaluation des futurs correctifs appliqués ultérieurement dans la séquence de mise à jour corrective. Plusieurs certificats peuvent exister dans la table, et le correctif doit correspondre à au moins un certificat à appliquer.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DisableLUAPatching](disableluapatching.md)
</dt> <dt>

[Mise à jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md)
</dt> <dt>

[**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
</dt> <dt>

[Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



