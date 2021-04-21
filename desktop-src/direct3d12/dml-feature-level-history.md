---
title: Historique des niveaux de fonctionnalité DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 68633f531c627eed8b02c7f65a248213743ca8bc
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803788"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="d0c11-103">Historique des niveaux de fonctionnalité DirectML</span><span class="sxs-lookup"><span data-stu-id="d0c11-103">DirectML feature level history</span></span>

<span data-ttu-id="d0c11-104">Pour un historique général des versions de DirectML, consultez [l’historique des versions DirectML](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="d0c11-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="d0c11-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="d0c11-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="d0c11-106">Introduit dans DirectML version 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="d0c11-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="d0c11-107">Ajout de la prise en charge des opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="d0c11-107">Added support for the following operators.</span></span>

* [<span data-ttu-id="d0c11-108">DML_OPERATOR_ELEMENT_WISE_ATAN_YX</span><span class="sxs-lookup"><span data-stu-id="d0c11-108">DML_OPERATOR_ELEMENT_WISE_ATAN_YX</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="d0c11-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="d0c11-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="d0c11-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="d0c11-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="d0c11-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="d0c11-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="d0c11-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="d0c11-114">Le nombre maximal de dimensions prises en charge pour les opérateurs suivants est passé de 4 à 8.</span><span class="sxs-lookup"><span data-stu-id="d0c11-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="d0c11-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="d0c11-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="d0c11-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="d0c11-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="d0c11-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="d0c11-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="d0c11-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="d0c11-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="d0c11-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="d0c11-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="d0c11-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="d0c11-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="d0c11-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="d0c11-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="d0c11-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="d0c11-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="d0c11-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="d0c11-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="d0c11-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="d0c11-127">Introduit dans DirectML version 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="d0c11-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="d0c11-128">Ajout de la prise en charge des opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="d0c11-128">Added support for the following operators.</span></span>

* [<span data-ttu-id="d0c11-129">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span><span class="sxs-lookup"><span data-stu-id="d0c11-129">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="d0c11-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="d0c11-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="d0c11-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="d0c11-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="d0c11-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="d0c11-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="d0c11-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="d0c11-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="d0c11-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="d0c11-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="d0c11-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="d0c11-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="d0c11-136">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="d0c11-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="d0c11-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="d0c11-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="d0c11-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="d0c11-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="d0c11-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="d0c11-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="d0c11-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="d0c11-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="d0c11-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="d0c11-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="d0c11-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="d0c11-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="d0c11-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="d0c11-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="d0c11-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="d0c11-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="d0c11-149">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0c11-149">Added the following enhancements.</span></span>

* <span data-ttu-id="d0c11-150">Le nombre maximal de dimensions de tenseur a été augmenté de 5 à 8.</span><span class="sxs-lookup"><span data-stu-id="d0c11-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="d0c11-151">Consultez [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d0c11-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="d0c11-152">Une prise en charge supplémentaire des types de données entiers a été ajoutée aux opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="d0c11-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="d0c11-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="d0c11-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="d0c11-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="d0c11-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="d0c11-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** et **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="d0c11-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="d0c11-156">**DML_OPERATOR_REDUCE**, lors de l’utilisation de **DML_REDUCE_FUNCTION_ARGMIN** ou **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="d0c11-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="d0c11-157">Les types de données 64 bits suivants ont été ajoutés et sont pris en charge par les opérateurs Select.</span><span class="sxs-lookup"><span data-stu-id="d0c11-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="d0c11-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="d0c11-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="d0c11-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="d0c11-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="d0c11-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="d0c11-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="d0c11-161">Fonctionnalités dépréciées.</span><span class="sxs-lookup"><span data-stu-id="d0c11-161">Deprecated functionality.</span></span>

* <span data-ttu-id="d0c11-162">**DML_REDUCE_FUNCTION_ARGMAX** et **DML_REDUCE_FUNCTION_ARGMIN** ont été dépréciés.</span><span class="sxs-lookup"><span data-stu-id="d0c11-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="d0c11-163">Il est préférable d’utiliser les opérateurs **DML_OPERATOR_ARGMIN** et **DML_OPERATOR_ARGMAX** autonomes à leur place.</span><span class="sxs-lookup"><span data-stu-id="d0c11-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="d0c11-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="d0c11-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="d0c11-165">Introduit dans DirectML version 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="d0c11-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="d0c11-166">Ajout des API suivantes.</span><span class="sxs-lookup"><span data-stu-id="d0c11-166">Added the following APIs.</span></span>

* [<span data-ttu-id="d0c11-167">Interface IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="d0c11-167">IDMLDevice1 interface</span></span>](./directml/nn-directml-idmldevice1.md)
* <span data-ttu-id="d0c11-168">Prise en charge des graphiques d’opérateur (consultez [IDMLDevice1 :: CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span><span class="sxs-lookup"><span data-stu-id="d0c11-168">Operator graph support (see [IDMLDevice1::CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span></span>

<span data-ttu-id="d0c11-169">Ajout de la prise en charge des opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="d0c11-169">Added support for the following operators.</span></span>

* <span data-ttu-id="d0c11-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="d0c11-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="d0c11-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="d0c11-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="d0c11-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="d0c11-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="d0c11-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="d0c11-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="d0c11-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="d0c11-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="d0c11-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="d0c11-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="d0c11-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="d0c11-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="d0c11-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="d0c11-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="d0c11-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="d0c11-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="d0c11-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="d0c11-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="d0c11-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="d0c11-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="d0c11-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="d0c11-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="d0c11-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="d0c11-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="d0c11-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="d0c11-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="d0c11-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="d0c11-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="d0c11-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="d0c11-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="d0c11-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="d0c11-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="d0c11-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="d0c11-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="d0c11-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="d0c11-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="d0c11-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="d0c11-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="d0c11-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="d0c11-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="d0c11-194">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0c11-194">Added the following enhancements.</span></span>

* <span data-ttu-id="d0c11-195">Une prise en charge supplémentaire des types de données entiers a été ajoutée aux opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="d0c11-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="d0c11-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="d0c11-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="d0c11-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="d0c11-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="d0c11-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="d0c11-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="d0c11-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="d0c11-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="d0c11-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="d0c11-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="d0c11-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="d0c11-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="d0c11-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="d0c11-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="d0c11-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="d0c11-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="d0c11-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="d0c11-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="d0c11-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="d0c11-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="d0c11-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="d0c11-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="d0c11-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="d0c11-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="d0c11-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="d0c11-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="d0c11-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="d0c11-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="d0c11-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="d0c11-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="d0c11-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="d0c11-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="d0c11-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="d0c11-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="d0c11-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="d0c11-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="d0c11-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="d0c11-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="d0c11-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="d0c11-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="d0c11-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="d0c11-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="d0c11-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="d0c11-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="d0c11-221">**DML_OPERATOR_TOP_K** et **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="d0c11-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="d0c11-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="d0c11-223">**DML_OPERATOR_REDUCE**, lors de l’utilisation de l’une des fonctions de réduction suivantes.</span><span class="sxs-lookup"><span data-stu-id="d0c11-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="d0c11-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="d0c11-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="d0c11-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="d0c11-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="d0c11-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="d0c11-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="d0c11-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="d0c11-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="d0c11-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="d0c11-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="d0c11-230">Restrictions de forme de tenseur souple pour **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="d0c11-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="d0c11-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="d0c11-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="d0c11-232">Introduit dans DirectML version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="d0c11-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="d0c11-233">Ajout des API suivantes.</span><span class="sxs-lookup"><span data-stu-id="d0c11-233">Added the following APIs.</span></span>
* [<span data-ttu-id="d0c11-234">Fonction DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="d0c11-234">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="d0c11-235">Énumération DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="d0c11-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="d0c11-236">Requêtes au niveau des fonctionnalités (voir [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="d0c11-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="d0c11-237">Ajout de la prise en charge des opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="d0c11-237">Added support for the following operators.</span></span>

* <span data-ttu-id="d0c11-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="d0c11-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="d0c11-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="d0c11-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="d0c11-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="d0c11-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="d0c11-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="d0c11-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="d0c11-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="d0c11-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="d0c11-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="d0c11-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="d0c11-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="d0c11-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="d0c11-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="d0c11-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="d0c11-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="d0c11-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="d0c11-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="d0c11-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="d0c11-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="d0c11-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="d0c11-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="d0c11-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="d0c11-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="d0c11-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="d0c11-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="d0c11-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="d0c11-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="d0c11-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="d0c11-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="d0c11-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="d0c11-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="d0c11-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="d0c11-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="d0c11-257">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0c11-257">Added the following enhancements.</span></span>

* <span data-ttu-id="d0c11-258">Lors de la liaison d’une ressource d’entrée pour la distribution d’un [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), il est maintenant légal de fournir une ressource avec [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (en plus de **D3D12_HEAP_TYPE_DEFAULT**), à condition que les propriétés de tas appropriées soient également définies.</span><span class="sxs-lookup"><span data-stu-id="d0c11-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="d0c11-259">Consultez [liaison dans DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="d0c11-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="d0c11-260">Les opérateurs booléens logiques suivants prennent désormais en charge les dizaines de temps de sortie **UINT8** , en plus de la prise en charge existante de **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="d0c11-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="d0c11-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="d0c11-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="d0c11-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="d0c11-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="d0c11-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="d0c11-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="d0c11-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="d0c11-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="d0c11-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="d0c11-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="d0c11-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="d0c11-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="d0c11-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="d0c11-268">5J les fonctions d’activation prennent désormais en charge l’utilisation de Strides sur leurs dizaines d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="d0c11-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="d0c11-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="d0c11-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="d0c11-270">Niveau de fonctionnalité dans lequel DirectML a été introduit.</span><span class="sxs-lookup"><span data-stu-id="d0c11-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0c11-271">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0c11-271">See also</span></span>

* [<span data-ttu-id="d0c11-272">Historique des versions DirectML</span><span class="sxs-lookup"><span data-stu-id="d0c11-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="d0c11-273">Énumération DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="d0c11-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="d0c11-274">Fonction DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="d0c11-274">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="d0c11-275">Structure DML_FEATURE_QUERY_FEATURE_LEVELS</span><span class="sxs-lookup"><span data-stu-id="d0c11-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)